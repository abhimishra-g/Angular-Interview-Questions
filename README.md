# Angular-Interview-Questions
**Q: How to set ngfor and ngif in the same div or tag?**  
**A**: Angular v2 doesn't support more than one structural directive on the same element. As a workaround use the `<ng-container>` OR `<ng-template>` element that allows you to use separate elements for each structural directive, but it is not stamped to the DOM.
<pre>   
    <ng-container *ngIf="condition">        
        <div *ngFor="let item of items">    
                <span>  
                    {{item}}    
                </span>
            </div>
        </ng-container>
    </pre>

**Q: What is the difference between AOT and JIT? What is the advantage of AOT?**    
**A**: Every Angular application consists of components and templates which the browser cannot understand. Therefore, all the Angular applications need to be compiled first before running inside the browser.
Angular provides two types of compilation:  
JIT(Just-in-Time) compilation   
AOT(Ahead-of-Time) compilation
