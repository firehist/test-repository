# Angular courses app

List all our challenges for this Angular course

Source code at each step is available through branches ====> [HERE](https://github.com/firehist/angular-courses-app/branches/yours)

## 00 - Introduction

Not really a challenge but it's an 'How To' bootstrap the app.

<details>
<summary>Click here to expand steps</summary>

### Install NVM (if wanted

1. Install NVM (https://github.com/creationix/nvm#install-script)
2. Install a Node Version through NVM
```
nvm install 7
nvm alias default 7
```

### Ensure node is installed w/ npm

```
$ node -v
v8.1.0
$ npm -v
5.0.3
```

### Install [@angular/cli](https://cli.angular.io) globally

`npm install -g @angular/cli

### Boostrap an angular cli application (updated guide on official website https://cli.angular.io)
```
ng new myProjectName
cd myProjectName
# Run the application through http://localhost:4200
ng serve
```

</details>


Proposed solution: [step-00](https://github.com/firehist/angular-courses-app/tree/step-00)

## 01 - Introduction to Components

**Main idea: use ng generate and be familiar with basic component**

Based on [step-00](https://github.com/firehist/angular-courses-app/tree/step-00)

Proposed solution: [step-01](https://github.com/firehist/angular-courses-app/tree/step-01)

<details>
<summary>Click here to expand steps</summary>

1. Create a component called `header`

```
$ ng generate component header
```

2. Add the selector element `<app-header></<app-header>` into the main HTML `app.component.html`
3. Play with template to see what's going on

- Add [ngx-bootstrap](https://github.com/valor-software/ngx-bootstrap/blob/development/docs/getting-started/ng-cli.md) or [angular2-materialize](https://github.com/InfomediaLtd/angular2-materialize#installing--configuring-angular2-materialize-in-projects-created-with-the-angular-cli)
- Design a navbar header to display the name of app and links for future routes
- Add code between `<app-header>` and `</<app-header>`
- be genious :D

</details>

## 02 - Templates, Interpolation & Directives

**Create a product list view by using ngIf & ngFor directives**

Based on [step-01](https://github.com/firehist/angular-courses-app/tree/step-01)

Proposed solution: [step-02](https://github.com/firehist/angular-courses-app/tree/step-02)

<details>
<summary>Click here to expand steps</summary>

1. Create a component called `product-list`

```
ng generate component product/product-list
```

2. Inject the created component into the `app.component.html`

```
<app-product-list></app-product-list>
```

3. Now, add an default products list into our `ProductListComponent` class (find below a default products array)

  ```
  products = [
        {
            "id": 1,
            "productName": "Leaf Rake",
            "productCode": "GDN-0011",
            "releaseDate": "March 19, 2016",
            "description": "Leaf rake with 48-inch wooden handle.",
            "price": 19.95,
            "starRating": 3.2,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/26215/Anonymous_Leaf_Rake.png"
        },
        {
            "id": 2,
            "productName": "Garden Cart",
            "productCode": "GDN-0023",
            "releaseDate": "March 18, 2016",
            "description": "15 gallon capacity rolling garden cart",
            "price": 32.99,
            "starRating": 4.2,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/58471/garden_cart.png"
        },
        {
            "id": 5,
            "productName": "Hammer",
            "productCode": "TBX-0048",
            "releaseDate": "May 21, 2016",
            "description": "Curved claw steel hammer",
            "price": 8.9,
            "starRating": 4.8,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/73/rejon_Hammer.png"
        },
        {
            "id": 8,
            "productName": "Saw",
            "productCode": "TBX-0022",
            "releaseDate": "May 15, 2016",
            "description": "15-inch steel blade hand saw",
            "price": 11.55,
            "starRating": 3.7,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/27070/egore911_saw.png"
        },
        {
            "id": 10,
            "productName": "Video Game Controller",
            "productCode": "GMG-0042",
            "releaseDate": "October 15, 2015",
            "description": "Standard two-button video game controller",
            "price": 35.95,
            "starRating": 4.6,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/120337/xbox-controller_01.png"
        }
    ]
  ```

4. Work on the product-list component template
    - Add a table to display product (display image url as text)
  
    - Use `*ngIf` directive to show the table if there is no product in the array
  
    - Use `*ngFor` directive on `<tr>` element to repeat this element as many times as products in the array
  
5. Bonus: Create a ProductListDetail component to replace HTML code of `*ngFor`

</details>

## 03 - Data Binding & Pipes

**Use property binding, event binding and two-way binding by using `[attr]`, `(event)` and `[(ngModel)]`**

Based on [step-02](https://github.com/firehist/angular-courses-app/tree/step-02)

Proposed solution: [step-03](https://github.com/firehist/angular-courses-app/tree/step-03)

<details>
<summary>Click here to expand steps</summary>

1. Display image as `<img src...` into the table with a *property binding* to `product.imageUrl` 
2. Add a button to show/hide all images on the page (you can handle click by using `<button (click)="myPublicMethod()"></button>`)
The text should be adapted to the current stage: `Show the images` or `Hide the images`
3. Set-up using banana in the box `[()]` the `ngModel` on the filter input text (two-way binding)
4. Create a custom Pipe to reverse a word & use it to display the filter text value.

</details>

## 04 - More on components

**Work around component lifecycle**

Based on [step-03](https://github.com/firehist/angular-courses-app/tree/step-03)

Proposed solution: [step-04](https://github.com/firehist/angular-courses-app/tree/step-04)

<details>
<summary>Click here to expand steps</summary>

1. Develop the `product` pipe and use it into the product-list view (to filter products array).
2. Use Component lifecycle to `console.log` a message into the `onInit` event
3. Add specific style for the product-list component
4. Add pipe to products `*ngFor` (eg: currency, uppercase, etc.)

</details>

### BONUS

Proposed solution: [step-04-bonus](https://github.com/firehist/angular-courses-app/tree/step-04-bonus)

<details>
<summary>Click here to expand bonus steps</summary>

Filter products without pipe. And add rating sort and so on.

</details>

## 05 - Building Nested Component

**Create a star component**

Based on [step-04](https://github.com/firehist/angular-courses-app/tree/step-04)

Proposed solution: [step-05](https://github.com/firehist/angular-courses-app/tree/step-05)

<details>
<summary>Click here to expand steps</summary>

1. Create a `starComponent` which display the rating with stars
2. Use this component into our `productListComponent` and place it next to existing `product.starRating`
3. Set-up `rating` input into `starComponent`
4. Set-up `ratingClicked` output into `starComponent`
5. Listen `ratingClicked` event from `ProductListComponent`

</details>

## 06 - Services and dependency injection

Based on [step-05](https://github.com/firehist/angular-courses-app/tree/step-05)

Proposed solution: [step-06](https://github.com/firehist/angular-courses-app/tree/step-06)

<details>
<summary>Click here to expand steps</summary>

1. Create a new angular service called `ProductService`

`$ ng generate service shared/models/product`

2. Ensure that it will be declared at our appModule level
3. Move the IProduct interface and the products array from our `productListComponent` to this new service
4. Write a public `getProducts` method to access to this products array

</details>

**BONUS**: Start to work with Observable

## 07 - Retrieving data Using HTTP

**Move products into a dedicated service**

Based on [step-06](https://github.com/firehist/angular-courses-app/tree/step-06)

Proposed solution: [step-07](https://github.com/firehist/angular-courses-app/tree/step-07)

<details>
<summary>Click here to expand steps</summary>

### Install json-server as fake backend server

1. Instal [`json-server`](https://github.com/typicode/json-server) package

```
npm install --server json-server
```

2. Create a folder `server`
3. Create a file into created folder called `db.json` with following content

```
{
    "products": [
        {
            "id": 1,
            "productName": "Leaf Rake",
            "productCode": "GDN-0011",
            "releaseDate": "March 19, 2016",
            "description": "Leaf rake with 48-inch wooden handle.",
            "price": 19.95,
            "starRating": 3.2,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/26215/Anonymous_Leaf_Rake.png"
        },
        {
            "id": 2,
            "productName": "Garden Cart",
            "productCode": "GDN-0023",
            "releaseDate": "March 18, 2016",
            "description": "15 gallon capacity rolling garden cart",
            "price": 32.99,
            "starRating": 4.2,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/58471/garden_cart.png"
        },
        {
            "id": 3,
            "productName": "Hammer",
            "productCode": "TBX-0048",
            "releaseDate": "May 21, 2016",
            "description": "Curved claw steel hammer",
            "price": 8.9,
            "starRating": 4.8,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/73/rejon_Hammer.png"
        },
        {
            "id": 4,
            "productName": "Saw",
            "productCode": "TBX-0022",
            "releaseDate": "May 15, 2016",
            "description": "15-inch steel blade hand saw",
            "price": 11.55,
            "starRating": 3.7,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/27070/egore911_saw.png"
        },
        {
            "id": 5,
            "productName": "Video Game Controller",
            "productCode": "GMG-0042",
            "releaseDate": "October 15, 2015",
            "description": "Standard two-button video game controller",
            "price": 35.95,
            "starRating": 4.6,
            "imageUrl": "http://openclipart.org/image/300px/svg_to_png/120337/xbox-controller_01.png"
        }
    ]
}
```
4. Edit the `package.json` file and add into `scripts` section the following line

```
"api": "json-server --watch ./server/db.json"
```

5. Then you can run your backend server by type the following command and enjoy http://localhost:3000

```
npm run api
```

#### Just Do It!

1. Import the `HttpModule` into the `AppModule` (if not already done)

    1. Install the `@angular/http` module
    2. Import the `HttpModule` into our `AppModule`

2. Inject `Http` into our `ProductService`
3. Update the `getProducts()` method to make a `get` call to our API Service `http://localhost:3000/products`
4. Use `RxJS` methods:

    1. `map` to convert the string result into a JSON Object
    2. `do` to `console.log` the JSON Object
    3. `catch` to attach a method to handle errors
    4. Imports
    
```
import { Observable } from 'rxjs/Observable'
import 'rxjs/add/operator/mergeMap';
```

5. Change into `ProductListComponent` the way we retrieve the data from our `ProductService`

</details>

#### BONUS: Do it with BehaviorSubject and Observables

Proposed solution: [step-07-bonus](https://github.com/firehist/angular-courses-app/tree/step-07-bonus)

## 08 - Navigation and Routing Basics

**Set-up basic routes to navigate across the application**

Based on [step-07](https://github.com/firehist/angular-courses-app/tree/step-07)

Proposed solution: [step-08](https://github.com/firehist/angular-courses-app/tree/step-08)

<details>
<summary>Click here to expand steps</summary>

We'll create 3 main routes: `/welcome`, `/products` and `/products/:id`.

1. Import the `RouterModule` into the `AppModule` (if not already there)

    - Install the `@angular/router` module

    ```
    $ npm install --save @angular/router
    ```

    - Import the `RouterModule` into our `AppModule` from installed package
    - Use the `RouterModule.forRoot([])` syntax to describe the application's routes (Note that `RouterModule.forChild([])` is used in angular sub-module of our application to avoid colision)

2. Create a basic `ProductDetailComponent` and a `WelcomeComponent` with angular cli

```
$ ng generate component modules/welcome
$ ng generate component modules/product/product --flat=true
$ ng generate component modules/product/product-detail
```

3. Create manually a ts file `./src/app/app.routes.ts` to centralize application routes and set-up our 3 routes: `/welcome`, `/products` and `/products/:id`. In order to organize routes, split products routes into a separated file `./.src/app/modules/product/product.routes.ts` with the same syntax.

```
import { Routes } from '@angular/router';

export const APP_ROUTES: Routes = [
    // Routes
]
```

4. Add the `<router-outlet></router-outlet>` directive into our `app.component.html` and `modules/product/product.component.html` to place views
5. Replace `RouterModule.forRoot([])` into `app.module.ts` to use the routes

```
import { APP_ROUTES } from './app.routes.ts`

// Some code ...

RouterModule.forRoot(APP_ROUTES)
```

6. Replace links into the top bar by using the directive `routerLink` directive and `routerLinkActive` to set style on current active link!
7. Replace links into our `ProductListComponent` in order to go to the detail page
8. Add a back button to the `ProductDetailComponent`.

```
<button routerLink="../">Back to products</button>
```

</details>

## 09 - Navigating and Routing Advanced

**Enhance our routes to read parameters, set-up guard and resolve data**

Based on [step-08](https://github.com/firehist/angular-courses-app/tree/step-08)

Proposed solution: [step-09](https://github.com/firehist/angular-courses-app/tree/step-09)

<details>
<summary>Click here to expand steps</summary>

1. Write a `getProduct(id: number): Observable<IProduct>` method into our `ProductService`

- This method looks like the existing `getProducts(): Observable<Array<IProduct>>` method
- Call the following URL instead: `http://localhost:3000/product/ID` where `ID` is the requested product id

2. Set-up a **resolve** called `product` in order to get the product object (`IProduct`)  into our `ProductDetailComponent`

- Create a new file injectable called `product.resolve.ts`

```
$ ng generate service shared/resolves/product-resolve
```

- Refactor the class name from `ProductResolveService` to `ProductResolve` & the filename from `product-resolve.service.ts` into `product.resolve.ts`
- Import the `ProductResolve` class into the `app.module.ts` file and add it into the `providers: []` array
- The class must implement the interface `Resolve<T>` imported from the `@angular/router` module
- This interface force you to write a method

```
class ProductResolve implements Resolve<T> {

    resolve(route: ActivatedRouteSnapshot, state: RouterStateSnapshot): Observable<T> | Promise<T> | T {
        // Your code can return an Observable, a Promise or T (T is a generic type, can be number, string, IProduct, etc.)
        // Here T is IProduct
    }

}
```

- Now, we'll write the body of this function

    - Retrieve id from URL params
    - Return the `getProduct(id)` from our `ProductService` to get our `Observable<IProduct>`

3. Add the resolve to the wanted route, here into the `product.routes.ts`

```
{ path: ':id', component: ProductDetailComponent, resolve: {
    product: ProductResolve
} }
```

*Here you should see when navigating to this route, a request sent to your server!*

4. Retrieve the `Observable<IProduct>` into our `ProductDetailComponent`

- Import & Inject the `ActivatedRoute` from `@angular/router`

```
import { ActivatedRoute } from '@angular/router';
// …
class ProductDetailComponent implements OnInit {
    constructor(private _route: ActivatedRoute) {} 
}
```

- Retrieve the `data` observable from `ActivatedRoute` and assign it to a class variable called `product$`

```
this.product$ = this._route.data.map(data => data.product)
```

5. Design the `ProductDetailComponent` HTML in order to display our `product$` information.  Use the pipe `async` into the `*ngIf`

```
<div *ngIf="product$ | async; let product; else noProductTemplate">
    ID: {{ product.id }}
</div>
<ng-template #noProductTemplate>
    <h4>No product found!</h4>
</ng-template>
```

6. Set-up into the HTML a button to go to the next product id (`product.id++`)

7. Set-up a **guard** to check if the given id is a number

- Generate a guard by using ng cli

```
$ ng generate guard --module app.module shared/guards/product-id
// --module will provide automatically the created file into our app.module.ts
```

- Update the code in order to check that the id param is well a number. Display a `console.error` else and redirect to the product list route

```
canActivate(
    next: ActivatedRouteSnapshot,
    state: RouterStateSnapshot): Observable<boolean> | Promise<boolean> | boolean {
    const id = Number(next.params.id)
    if (isNaN(id) || id > 0) {
        // console.error & redirect
    }
    return true
}
```

- Add the guard to the wanted route, here into the `product.routes.ts`

```
{ path: ':id', component: ProductDetailComponent, resolve: {
    product: ProductResolve
}, canActivate: [ProductIdGuard] }
```

Here we go! 👌

**Resolve**: It prepares our data for the targeted component

**Guard**: It active/deactive a route based on custom check (here that the id is a number)

</details>

## 10 - Forms

**Edit/Create a product by using forms**

Based on [step-09](https://github.com/firehist/angular-courses-app/tree/step-09)

Proposed solution: [step-10](https://github.com/firehist/angular-courses-app/tree/step-10)

<details>
<summary>Click here to expand steps</summary>

1. Import @angular modules `FormsModule` & `ReactiveFormsModule`

- Install npm package `@angular/forms`

```
$ npm install --save @angular/forms
```

- Import `FormsModule` & `ReactiveFormsModule` from `@angular/forms` into the app.module file

```
import { Formsmodule, ReactiveFormsModule } from '@angular/forms';
// …
@ngModule({
    //…
    imports: […, FormsModule, ReactiveFormsModule]
})
```

2. Display a form to feed all fields about product in HTML template (in `ProductDetailComponent`)

    - You can use ngIf/else syntax

```
<div *ngIf="myTest; else toto">
  // Displayed if myTest
</div>
<ng-template #toto>
  // Displayed else
</ng-template>
```

4. Create the forms in `model driven` way into the component

- Import useful artefact from `@angular/forms`: `FormBuilder`, `FormGroup`, `Validators`
- Inject the `FormBuilder`
- Design the form into the constructor

```
this.myForm = this._formBuilder.group({
    id: '',
    productName: '',
    ... etc.
})
```

5. Create and connect the HTML form to the JS FormGroup by using these directives: `FormGroup`, `FormControlName`

```
<form [formGroup]="myForm">
    //…
    <input type="text" formControlName="productName" />
    //…
</form>
```

6. Display into the HTML a submit button which is disabled when the form is `INVALID`

```
<input type="submit" [disabled]="myForm.invalid" />
```

7. Change the input style based on [validation css rules](https://angular.io/guide/forms#track-control-state-and-validity-with-ngmodel)

- Create a folder `./src/styles`
- Create a file `./src/styles/form.css`

```
.ng-valid[required], .ng-valid.required  {
  border-left: 5px solid #42A948; /* green */
}

.ng-invalid:not(form)  {
  border-left: 5px solid #a94442; /* red */
}
```

- Import this new css file into the `styles.css`

```
@import url(styles/form.css);
```

8. Write the submit method in order to save the product through a call to our server

- Create a method `saveProduct(product: IProduct): Observable<IProduct>` into our `ProductService`.

```
return this._http.put(url, payload)
    //…
```

- Create a method `onSubmit()` into our `ProductDetailComponent` in order to manage the form submission.

```
submit() {
    if (this.formProduct.valid) {
        this._productService.saveProduct(this.formProduct.value)
            .subscribe(newProduct => {      // Here we subscribe to do the request
                this.product$ = Observable.from([product])  // We create a new observable from the server response to update our product
                this.toggleMode()
            })
    }
}
```

- Into the `ProductDetailTemplate`, write a submit button, disabled if the form is invalid

```
<button type="submit" [disabled]="productForm.invalid">Save</button>
```

</details>

### WARNING

Here, we update the product into our component. It works like a charm 'cause we don't display information of this product concurrently in an other part of the view.

If for example, we display current product name into the navbar, after a save, data will be different as we refresh only the `ProductDetailComponent` product information.

In order to fix that, you cake a look to [step-07-bonus](https://github.com/firehist/angular-courses-app/tree/step-07-bonus) which, instead of returns Observables from angular `Http` service, will manage a collection in-memory and always returns this Observable, with or without filter.

It will allow all our component to be aware of any change on this collection!

We'll do this fix into **11 - Advanced forms**

## 11 - Advanced forms

Based on [step-10](https://github.com/firehist/angular-courses-app/tree/step-10)

Proposed solution: [step-11](https://github.com/firehist/angular-courses-app/tree/step-11)

<details>
<summary>Click here to expand steps</summary>

1. Update our `ProductService` to manage a collection in-memory

Use [step-07-bonus](https://github.com/firehist/angular-courses-app/tree/step-07-bonus)

```
class ProductService {

    private products$: BehaviorSubject(Array<IProduct>) = new BehaviorSubject<Array<IProduct>>([])
    private dataStore = {
        products: []
    }

    constructor(private _http: HttpService) {
        this._next() // Emit the dataStore.products event
    }

    getAll() {
        // 1. Do the request call by subscribing
        this._http.get(`URL`).map(res => res.json())
            .subscribe(products => {
                // 2. Sync our dataStore
                this.syncProducts(products)
            })
        // 3. Return the BehaviorSubject as Observable
        return this.products$.asObservable()
    }

    get(id: number) {
        // 1. Same as getAll for one product
        // 2. call _syncProduct instead of _syncProducts
        // 3. Return the BehaviorSubjected as Observable with filter to get the product
        return this.products$.asObservable()
            .flatMap(products => products) // Flatten the Array<IProduct>
            .filter(product => product.id === id)
    }

    private _syncProducts(products: Array<IProduct>) {
        this.dataStore.products = products
        this._next()
    }

    private _syncProduct(product: IProduct) {
        this.dataStore.products.map(storeProduct => {
            return storeProduct.id === product.id ?
                product : storeProduct
        })
        this._next()
    }

    private _next() {
        this.products$.next(this.dataStore.products)
    }

}
```

2. Create a [custom Validator](https://angular.io/guide/form-validation#custom-validation)

- Create an empty file into `./src/app/shared/validators/product.validators.ts`
- Write validator functions into it

```
export function validProductCode(control:AbstractControl): {[key: string]: any} => {
    const productRegex = /[A-Z]{3}-[0-9]{4}/
    const productCode = control.value
    return productRegex.test(value) ? {'validProductCode': {productCode}} : null;
}

// Function below coming from angular spec
export function forbiddenNameValidator(nameRe: RegExp): ValidatorFn {
  return (control: AbstractControl): {[key: string]: any} => {
    const name = control.value;
    const no = nameRe.test(name);
    return no ? {'forbiddenName': {name}} : null;
  };
}
```

- Add `validProductCode` to the `productCode` validators Array into our form

```
import { validProductCode } from '../../shared/validators/product.validators.ts'
//…
productCode: ['', validProductCode]
```

- Add `forbiddenNameValidator` to the `productName` to block a regex (eg: blocked)

```
import { forbiddenNameValidator } from '../../shared/validators/product.validators.ts'
//…
productName: ['', [//…, forbiddenNameValidator(/blocked/)]]
```

3. Display error messages

```
<div *ngIf="productForm.get('productCode').errors?.validProductCode" class="alert alert-danger">
    Invalid product code.
</div>
```

</details>

## 12 - Reactive Programming

No challenge here!

## 13 - Angular 2 set-up revisited

No challenge here!

## 14 - Unit Testing w/ Jasmine & Karma

No challenge here!

## 15 - Data Store with @ngrx/store

No challenge here!
