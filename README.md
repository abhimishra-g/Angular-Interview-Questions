# Angular-Interview-Questions
**Q: How to set ngfor and ngif in the same div or tag?**  
**A**: Angular v2 doesn't support more than one structural directive on the same element. As a workaround use the `<ng-container>` OR `<ng-template>` element that allows you to use separate elements for each structural directive, but it is not stamped to the DOM.     
    `<ng-container *ngIf="condition">`    
    `<div *ngFor="let item of items">`    
    `<span>`    
    `{{item}}`    
    `</span>`    
    `</div>`    
    `</ng-container>`    

**Q: What is the difference between AOT and JIT? What is the advantage of AOT?**    
**A**: Every Angular application consists of components and templates which the browser cannot understand. Therefore, all the Angular applications need to be compiled first before running inside the browser.
Angular provides two types of compilation:  
    JIT(Just-in-Time) compilation   
    AOT(Ahead-of-Time) compilation    
In JIT compilation, the application compiles inside the browser during runtime. Whereas in the AOT compilation, the application compiles during the build time.    
The advantages of using AOT compilation are:    
Since the application compiles before running inside the browser, the browser loads the executable code and renders the application immediately, which leads to faster rendering.    
In AOT compilation, the compiler sends the external HTML and CSS files along with the application, eliminating separate AJAX requests for those source files, which leads to fewer ajax requests.    
Developers can detect and handle errors during the building phase, which helps in minimizing errors.    
The AOT compiler adds HTML and templates into the JS files before they run inside the browser. Due to this, there are no extra HTML files to be read, which provide better security to the application.
