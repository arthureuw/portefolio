---
title: 'Angular : Build Reactive Forms with Bootstrap 4'
---

First of all i'm going to add `ReactiveFormsModule` in the `app.module.ts`

```javascript
import { ReactiveFormsModule } from '@angular/forms';

@NgModule({
  declarations: [...],
  imports: [
    ReactiveFormsModule
  ],
  bootstrap: [...]
})

export class AppModule { }
```  
---
Then i create a form with **Bootstrap 4** and **Reactive Forms APIs** in the `app/form.component.html.

```html
<div class="container">
  <form [formGroup]="form" (ngSubmit)="submitForm()">
    <div class="form-group input-group-lg">
      <input class="form-control" placeholder="McDonald's" formControlName="name">
    </div>

    <div class="form-group input-group-lg">
      <input class="form-control" placeholder="Fast Food" formControlName="type">
    </div>

    <div class="form-group">
      <button class="btn btn-danger btn-block btn-lg">Create</button>
    </div>
  </form>
</div>
```  
---
Next step will be in the `app/form.component.ts` file, i add the following code :
```typescript 
import { Component, OnInit } from '@angular/core';
import { FormBuilder, FormGroup } from "@angular/forms";

@Component({
  selector: 'app-form',
  templateUrl: './form.component.html',
  styleUrls: ['./form.component.css']
})

export class FormComponent implements OnInit {
  form: FormGroup;

  constructor(public fb: FormBuilder) {
    this.form = this.fb.group({
      name: [''],
      type: ['']
    })
  }

  ngOnInit() { }

  submitForm() {
    console.log(this.form.value)
  }

}
```
---   
#### Uploading picture with your brand new form ?  

If you want to Upload picture from your form you'll just have to add the next line to your `form.component.ts`
```typescript
  uploadFile(event) {
    const file = (event.target as HTMLInputElement).files[0];
    this.form.patchValue({
      avatar: file
    });
    this.form.get('avatar').updateValueAndValidity()
  }
```
and this to your `form.component.html`.
```html
<input type="file" (change)="uploadFile($event)">
```