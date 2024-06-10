<h1>Angular Forms</h1> - https://medium.com/@jaydeepvpatil225/forms-in-angular-8fde7d0dcdf6

- In Angular, Forms provides a set of features that help us handle and manage user input in a structured and efficient manner.
- Forms are the main part of web applications that allow users to interact with the application and submit data to the application.

<h2>Types of Forms in Angular</h2>

Angular provides the following two types of forms:

1. Template-Driven Forms
2. Reactive Forms

<h3>1. Template-Driven Forms</h3>

- Template-driven forms are the basic forms that are suitable for the development of a limited number of fields and with simpler validation
-  In this form, each field is represented as a property in the component class.
-  You Need to import **FormsModule** from the `@angular/forms` package.

Following are the key concepts related to validation objects, directives, and properties that we used while creating the template-driven forms in Angular:

**ngForm Directive:** This directive represents an angular form and exposes methods and properties related to it for validation and data manipulation purposes.

**ngModel Directive:** This directive is used to achieve two-way data bindings between different form control elements.

**Validation Properties:** Angular provides different validator properties that can be applied to form controls to indicate their validation state:

1. `touched`: A boolean indicating whether the control has been touched.
2. `untouched`: The opposite of touched.
3. `valid`: A boolean indicating whether the control’s value is valid.
4. `invalid`: The opposite of valid

**Validation Directives:** Angular provides several built-in validation directives that can be used with ngModel to perform validation. Some common ones include:

1. `required`: Ensures the control has a non-empty value.
2. `min length and max length`: Specifies the minimum and maximum length for the value.
3. `pattern`: Validates the value against a regular expression.
4. `email`: Validates that the value is a valid email address.

**Exaple:**
```html
<form #singUpForm="ngForm" (ngSubmit)="onSubmit(singUpForm)">

    <p>
        <label for="firstname">First Name</label>
        <input type="text" name="firstname" required minlength="20" ngModel>
    </p>

    <p>
        <label for="lastname">Last Name</label>
        <input type="text" name="lastname" pattern="^[a-zA-Z]+$" ngModel>
    </p>

    <p>
        <label for="email">Email </label>
        <input type="text" id="email" name="email" required email ngModel>
    </p>

    <p>
        <label for="gender">Geneder</label>
        <input type="radio" value="male" name="gender" ngModel> Male
        <input type="radio" value="female" name="gender" ngModel> Female
    </p>

    <p>
        <label for="isMarried">Married</label>
        <input type="checkbox" name="isMarried" ngModel>
    </p>

    <select name="country" ngModel>
        <option [ngValue]="c.id" *ngFor="let c of countryList">
            {{c.name}}
        </option>
    </select>

    <p>
        <button type="submit">Submit</button>
    </p>

</form>
```
```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
    title = 'Template driven forms';

    countryList: country[] = [
        new country("1", "Pakistan"),
        new country('2', 'UAE'),
        new country('3', 'USA')
    ];
}

export class country {
    id: string;
    name: string;

    constructor(id: string, name: string) {
        this.id = id;
        this.name = name;
    }

    onSubmit(contactForm: any) {
        console.log(contactForm.value);
    }

    //   OR

    @ViewChild('singUpForm') form: any;
    onSubmit() {
        if (this.form.valid) {
            console.log("Form Submitted!");
            this.form.reset();
        }
    }
}
```

<h2>2. Reactive Forms</h2>

- Reactive forms, or model-driven forms, are the types of forms in Angular that are suitable for creating a large form with different form fields and complex validation.
- In the reactive form, each form field is considered a Form Control, and a set of form controls is called a Form Group.
- The validation rules are defined in the component with the Validators object, and validation messages can be displayed in the template with the help of the validation property.
- ReactiveFormModule needs to be imported from the `@angular/forms` package.

Following are the key concepts related to validation objects and properties that we used while creating the reactive forms in Angular:

**FormControl**

In Angular, form control represents individual form elements in the reactive form. It also manages the different states and values of input form elements. It has different properties with which we can define validation rules.

1. **Value**: It helps us check the current value of the form control.
2. **Status**: Status represents the state of the form control.
3. **Valid**: It is the boolean validation property that checks whether the control is valid.
4. **Invalid**: It is the boolean validation property that checks whether the control is invalid.
5. **Errors**: It’s the object that holds validation errors for the form control.

**Validators**

Validators are functions that you can use to define validation rules for form controls.

1. **required**: Validates that the control has a non-empty value.
2. **Min and max**: Validate that the control value is within a specified numeric range.
3. **pattern**: Validates the control value against a regular expression.
4. **email**: Validates that the control value is a valid email address.
5. **minLength and maxLength**: Validate the length of the control value.

**FormGroup**

A form group is a container for multiple form controls. It allows you to group related form controls together and manage their validation as a single unit.

**FormBuilder**

The FormBuilder service is used for creating instances of FormGroup and FormControl while providing a convenient way to define validation rules.

**Example 1**

```html
<form class="pageContext" [formGroup]="formGroup">
    <li class="item-shhet-filter customerDetailsW">
        <mat-form-field class="po-select-field po-select-field-small" floatLabel="never">
        <mat-label>Customer Detail</mat-label>
        <mat-select formControlName="customerDetails" (selectionChange)="toggleCustomerDetails()" matInput multiple>
            <mat-select-trigger>Group ({{formGroup.get('customerDetails')?.value?.length}})</mat-select-trigger>
            <mat-option>
            <ngx-mat-select-search [placeholderLabel]="'Search...'" [noEntriesFoundLabel]="'no matching customer group found'"
                [toggleAllCheckboxChecked]="toggleAllCustomerDetailsCheckboxState" [showToggleAllCheckbox]="true"
                [formControl]="filterCtrlFormGroup.get('customerDetailsFilterCtrl')" (toggleAll)="toggleSelectAllCustomerDetails($event)">
            </ngx-mat-select-search>
            </mat-option>
            <ng-container *ngFor="let customer of customerDetailsListOptions">
            <mat-option [value]="customer?.customerId">
                ({{customer?.customerId}}) {{customer?.name}}
            </mat-option>
            </ng-container>
        </mat-select>
        </mat-form-field>
    </li>
    <li class="item-shhet-filter plantIdsW">
        <mat-form-field class="po-select-field po-select-field-small" floatLabel="never">
        <mat-label>Plant</mat-label>
        <mat-select formControlName="plantIds" (selectionChange)="togglePlantIds()" matInput multiple>
            <mat-select-trigger>Plant ({{formGroup.get('plantIds')?.value?.length}})</mat-select-trigger>
            <mat-option>
            <ngx-mat-select-search [placeholderLabel]="'Search...'" [noEntriesFoundLabel]="'no matching plant found'"
                [toggleAllCheckboxChecked]="toggleAllPlantIdsCheckboxState" [showToggleAllCheckbox]="true"
                [formControl]="filterCtrlFormGroup.get('plantIdsFilterCtrl')" (toggleAll)="toggleSelectAllPlantIds($event)">
            </ngx-mat-select-search>
            </mat-option>
            <ng-container *ngFor="let plant of plantIdsListOptions">
            <mat-option [value]="plant">
                {{plant}}
            </mat-option>
            </ng-container>
        </mat-select>
        </mat-form-field>
    </li>
    <li class="item-shhet-filter broadStagesW">
        <mat-form-field class="po-select-field po-select-field-small" floatLabel="never">
        <mat-label>Broad Stage</mat-label>
        <mat-select formControlName="broadStages" (selectionChange)="toggleBroadStages()" matInput multiple>
            <mat-select-trigger>Broad Stage ({{formGroup.get('broadStages')?.value?.length}})</mat-select-trigger>
            <mat-option>
            <ngx-mat-select-search [placeholderLabel]="'Search...'" [noEntriesFoundLabel]="'no matching broad stage found'"
                [toggleAllCheckboxChecked]="toggleAllBroadStagesCheckboxState" [showToggleAllCheckbox]="true"
                [formControl]="filterCtrlFormGroup.get('broadStagesFilterCtrl')" (toggleAll)="toggleSelectAllBroadStages($event)">
            </ngx-mat-select-search>
            </mat-option>
            <ng-container *ngFor="let broadStages of broadStagesListOptions">
            <mat-option [value]="broadStages">
                {{broadStages}}
            </mat-option>
            </ng-container>
        </mat-select>
        </mat-form-field>
    </li>
    <li class="item-shhet-filter prTypesW">
        <mat-form-field class="po-select-field po-select-field-small" floatLabel="never">
        <mat-label>PR Type</mat-label>
        <mat-select formControlName="prTypes" (selectionChange)="togglePrTypes()" matInput multiple>
            <mat-select-trigger>PR Types ({{formGroup.get('prTypes')?.value?.length}})</mat-select-trigger>
            <mat-option>
            <ngx-mat-select-search [placeholderLabel]="'Search...'" [noEntriesFoundLabel]="'no matching pr types found'"
                [toggleAllCheckboxChecked]="toggleAllPrTypesCheckboxState" [showToggleAllCheckbox]="true"
                [formControl]="filterCtrlFormGroup.get('prTypesFilterCtrl')" (toggleAll)="toggleSelectAllPrTypes($event)">
            </ngx-mat-select-search>
            </mat-option>
            <ng-container *ngFor="let prTypes of prTypesListOptions">
            <mat-option [value]="prTypes">
                {{prTypes}}
            </mat-option>
            </ng-container>
        </mat-select>
        </mat-form-field>
    </li>
    <li class="item-shhet-filter prAgingBucketsW">
        <mat-form-field class="po-select-field po-select-field-small" floatLabel="never">
        <mat-label>PR Aging Bucket</mat-label>
        <mat-select formControlName="prAgingBuckets" (selectionChange)="togglePrAgingBuckets()" matInput multiple>
            <mat-select-trigger>PR Aging Bucket ({{formGroup.get('prAgingBuckets')?.value?.length}})</mat-select-trigger>
            <mat-option>
            <ngx-mat-select-search [placeholderLabel]="'Search...'" [noEntriesFoundLabel]="'no matching pr aging buckets found'"
                [toggleAllCheckboxChecked]="toggleAllPrAgingBucketsCheckboxState" [showToggleAllCheckbox]="true"
                [formControl]="filterCtrlFormGroup.get('prAgingBucketsFilterCtrl')" (toggleAll)="toggleSelectAllPrAgingBuckets($event)">
            </ngx-mat-select-search>
            </mat-option>
            <ng-container *ngFor="let prAgingBuckets of prAgingBucketsListOptions">
            <mat-option [value]="prAgingBuckets">
                {{prAgingBuckets}}
            </mat-option>
            </ng-container>
        </mat-select>
        </mat-form-field>
    </li>
    <li class="item-shhet-filter sourcer1W">
        <mat-form-field class="po-select-field po-select-field-small" floatLabel="never">
        <mat-label>Sourcer 1</mat-label>
        <mat-select formControlName="sourcer1" (selectionChange)="toggleSourcer1()" matInput multiple>
            <mat-select-trigger>Sourcer 1 ({{formGroup.get('sourcer1')?.value?.length}})</mat-select-trigger>
            <mat-option>
            <ngx-mat-select-search [placeholderLabel]="'Search...'" [noEntriesFoundLabel]="'no matching pr sourcer1 found'"
                [toggleAllCheckboxChecked]="toggleAllSourcer1CheckboxState" [showToggleAllCheckbox]="true"
                [formControl]="filterCtrlFormGroup.get('sourcer1FilterCtrl')" (toggleAll)="toggleSelectAllSourcer1($event)">
            </ngx-mat-select-search>
            </mat-option>
            <ng-container *ngFor="let sourcer1 of sourcer1ListOptions">
            <mat-option [value]="sourcer1">
                {{sourcer1}}
            </mat-option>
            </ng-container>
        </mat-select>
        </mat-form-field>
    </li>
    <li class="item-shhet-filter sourcer2W">
        <mat-form-field class="po-select-field po-select-field-small" floatLabel="never">
        <mat-label>Sourcer 2</mat-label>
        <mat-select formControlName="sourcer2" (selectionChange)="toggleSourcer2()" matInput multiple>
            <mat-select-trigger>Sourcer 2 ({{formGroup.get('sourcer2')?.value?.length}})</mat-select-trigger>
            <mat-option>
            <ngx-mat-select-search [placeholderLabel]="'Search...'" [noEntriesFoundLabel]="'no matching pr sourcer2 found'"
                [toggleAllCheckboxChecked]="toggleAllSourcer2CheckboxState" [showToggleAllCheckbox]="true"
                [formControl]="filterCtrlFormGroup.get('sourcer2FilterCtrl')" (toggleAll)="toggleSelectAllSourcer2($event)">
            </ngx-mat-select-search>
            </mat-option>
            <ng-container *ngFor="let sourcer2 of sourcer2ListOptions">
            <mat-option [value]="sourcer2">
                {{sourcer2}}
            </mat-option>
            </ng-container>
        </mat-select>
        </mat-form-field>
    </li>
    <li class="item-shhet-filter DateW">
        <mat-form-field class="po-select-field-small dateSelection" floatLabel="never">
            <mat-select placeholder="Creation/Received Date" name="datetype" matInput
                formControlName="dateType">
                <ng-container *ngFor="let date of dateTypeList">
                    <mat-option [value]="date?.value">{{date?.view}}</mat-option>
                </ng-container>
            </mat-select>
        </mat-form-field>
        <mat-form-field class="po-select-field-small fordatePicker" floatLabel="never">
            <label class="cust_label"></label>
            <input type="text" [formControl]="formGroup.get('date')" matInput
                ngxDaterangepickerMd [autoApply]="dateRangePickerOptions.autoApply"
                [linkedCalendars]="dateRangePickerOptions.linkedCalendars"
                [singleDatePicker]="dateRangePickerOptions.singleDatePicker" applyLabel="Okay"
                [locale]="dateRangePickerLocale" [showDropdowns]="true" startKey="start" endKey="end"
                [showWeekNumbers]="dateRangePickerOptions.showWeekNumbers"
                [showCancel]="dateRangePickerOptions.showCancel"
                [showClearButton]="dateRangePickerOptions.showClearButton"
                [showISOWeekNumbers]="dateRangePickerOptions.showISOWeekNumbers"
                firstMonthDayClass="first-day" lastMonthDayClass="last-day"
                emptyWeekRowClass="empty-week" lastDayOfPreviousMonthClass="last-previous-day"
                firstDayOfNextMonthClass="first-next-day" name="daterange" />
        </mat-form-field>
    </li>
</form>
```
```ts
import { FormControl, FormGroup } from '@angular/forms';
import { distinctUntilChanged, startWith, Subject } from 'rxjs';

@Component({
  selector: 'app-pr-sheet',
  templateUrl: './pr-sheet.component.html',
  styleUrls: ['./pr-sheet.component.scss']
})
export class PrSheetComponent implements OnInit {

  globalFilterList: any = {};
  sheetGroupInfo: Array<any> = [];
  dateRangePickerOptions: any = {
    autoApply: false,
    alwaysShowCalendars: false,
    showCancel: false,
    showClearButton: false,
    linkedCalendars: true,
    singleDatePicker: false,
    showWeekNumbers: false,
    showISOWeekNumbers: false
  };
  dateRangePickerLocale: any = {
    format: 'MM/DD/YYYY',
    separator: ' - ',
    cancelLabel: 'Cancel',
    applyLabel: 'Okay'
  }
  customerDetailsListOptions: Array<any> = [];
  plantIdsListOptions: Array<string> = [];
  broadStagesListOptions: Array<string> = [];
  prTypesListOptions: Array<string> = [];
  prAgingBucketsListOptions: Array<string> = [];
  sourcer1ListOptions: Array<string> = [];
  sourcer2ListOptions: Array<string> = [];
  toggleAllCustomerDetailsCheckboxState: boolean = false;
  toggleAllPlantIdsCheckboxState: boolean = false;
  toggleAllBroadStagesCheckboxState: boolean = false;
  toggleAllPrTypesCheckboxState: boolean = false;
  toggleAllPrAgingBucketsCheckboxState: boolean = false;
  toggleAllSourcer1CheckboxState: boolean = false;
  toggleAllSourcer2CheckboxState: boolean = false;
  closePrItemIDs: any[];
  autocompleteListEvent = new Subject<any>();
  autocompleteList: Array<any> = [];
  hasRoleforDeletion: boolean;

  constructor() {
    this.initFormroup();
    this.initFilterCtrlFormGroup();
    this.getGlbalFilterList();
  }

  ngOnInit(): void {}

  initFormroup() {
    this.formGroup = new FormGroup({
      floatingSearchFilterKey: new FormControl(null),
      floatingSearchFilterValue: new FormControl(null),
      customerDetails: new FormControl([]),
      plantIds: new FormControl([]),
      broadStages: new FormControl([]),
      prTypes: new FormControl([]),
      prAgingBuckets: new FormControl([]),
      sourcer1: new FormControl([]),
      sourcer2: new FormControl([]),
      dateType: new FormControl('creationDate'),
      date: new FormControl({ start: moment.utc((new Date())).utcOffset(330).startOf('day').subtract(30, 'day'), end: moment.utc((new Date())).utcOffset(330).endOf('day') }),
    })
  }

  initFilterCtrlFormGroup() {
    this.filterCtrlFormGroup = new FormGroup({
      customerDetailsFilterCtrl: new FormControl(null),
      plantIdsFilterCtrl: new FormControl(null),
      broadStagesFilterCtrl: new FormControl(null),
      prTypesFilterCtrl: new FormControl(null),
      prAgingBucketsFilterCtrl: new FormControl(null),
      sourcer1FilterCtrl: new FormControl(null),
      sourcer2FilterCtrl: new FormControl(null),
    })
  }

  getGlbalFilterList() {
    this.poService.getPRSheetGloablFilterList().subscribe((res: any) => {
      if (res?.code == 200 && res?.success) {
        this.globalFilterList = res?.data?.filters?.prFilter;
        this.filterCtrlFormGroupValueChanges();
        this.applyFilter();
      } else {
        this.alertMessageService.addError(res?.message || MESSAGES.ERROR.SOMETHING_WENT_WRONG).show();
        this.applyFilter();
      }
    }, (err: any) => {
      this.alertMessageService.addError(MESSAGES.ERROR.SOMETHING_WENT_WRONG).show();
      this.applyFilter();
    })
  }

  filterCtrlFormGroupValueChanges() {
    this.filterCtrlFormGroup.valueChanges
      .pipe(startWith(''), distinctUntilChanged((prev: any, next: any) => JSON.stringify(prev) === JSON.stringify(next)))
      .subscribe((res) => {
        this.customerDetailsListOptions = this.globalFilterList?.customerDetails?.filter((customer: any) => (customer.customerId + customer?.name).toLowerCase().includes(this.filterCtrlFormGroup.get("customerDetailsFilterCtrl")?.value?.toString().toLowerCase().trim() || ""));
        this.plantIdsListOptions = this.globalFilterList?.plantIds?.filter((plant: number) => String(plant)?.includes(this.filterCtrlFormGroup.get("plantIdsFilterCtrl")?.value?.trim() || ""));
        this.broadStagesListOptions = this.globalFilterList?.broadStages?.filter((broadStages: string) => broadStages?.toLowerCase().includes(this.filterCtrlFormGroup.get("broadStagesFilterCtrl")?.value?.toString().toLowerCase().trim() || ""));
        this.prTypesListOptions = this.globalFilterList?.prTypes?.filter((prTypes: string) => prTypes?.toLowerCase().includes(this.filterCtrlFormGroup.get("prTypesFilterCtrl")?.value?.toString().toLowerCase().trim() || ""));
        this.prAgingBucketsListOptions = this.globalFilterList?.prAgingBuckets?.filter((prAgingBuckets: string) => prAgingBuckets?.toLowerCase().includes(this.filterCtrlFormGroup.get("prAgingBucketsFilterCtrl")?.value?.toString().toLowerCase().trim() || ""));
        this.sourcer1ListOptions = this.globalFilterList?.sourcer1?.filter((sourcer1: string) => sourcer1?.toLowerCase().includes(this.filterCtrlFormGroup.get("sourcer1FilterCtrl")?.value?.toString().toLowerCase().trim() || ""));
        this.sourcer2ListOptions = this.globalFilterList?.sourcer2?.filter((sourcer2: string) => sourcer2?.toLowerCase().includes(this.filterCtrlFormGroup.get("sourcer2FilterCtrl")?.value?.toString().toLowerCase().trim() || ""));
      })
  }

  toggleSelectAllCustomerDetails(event: any) {
    this.toggleAllCustomerDetailsCheckboxState = event;
    this.formGroup.get("customerDetails")?.patchValue(event ? this.globalFilterList?.customerDetails?.map((customer: any) => customer?.customerId) : [])
  }

  toggleSelectAllPlantIds(event: any) {
    this.toggleAllPlantIdsCheckboxState = event;
    this.formGroup.get("plantIds")?.patchValue(event ? this.globalFilterList?.plantIds : []);
  }

  toggleSelectAllBroadStages(event: any) {
    this.toggleAllBroadStagesCheckboxState = event;
    this.formGroup.get("broadStages")?.patchValue(event ? this.globalFilterList?.broadStages : []);
  }

  toggleSelectAllPrTypes(event: any) {
    this.toggleAllPrTypesCheckboxState = event;
    this.formGroup.get("prTypes")?.patchValue(event ? this.globalFilterList?.prTypes : []);
  }

  toggleSelectAllPrAgingBuckets(event: any) {
    this.toggleAllPrAgingBucketsCheckboxState = event;
    this.formGroup.get("prAgingBuckets")?.patchValue(event ? this.globalFilterList?.prAgingBuckets : []);
  }

  toggleSelectAllSourcer1(event: any) {
    this.toggleAllSourcer1CheckboxState = event;
    this.formGroup.get("sourcer1")?.patchValue(event ? this.globalFilterList?.sourcer1 : []);
  }

  toggleSelectAllSourcer2(event: any) {
    this.toggleAllSourcer2CheckboxState = event;
    this.formGroup.get("sourcer2")?.patchValue(event ? this.globalFilterList?.sourcer2 : []);
  }

  toggleCustomerDetails() {
    this.toggleAllCustomerDetailsCheckboxState = JSON.stringify(this.formGroup.get("customerDetails")?.value?.sort()) == JSON.stringify(this.globalFilterList?.customerDetails?.map((customer: any) => customer?.customerId)?.sort());
  }

  togglePlantIds() {
    this.toggleAllPlantIdsCheckboxState = JSON.stringify(this.formGroup.get("plantIds")?.value?.sort()) == JSON.stringify(this.globalFilterList?.plantIds?.sort());
  }

  toggleBroadStages() {
    this.toggleAllBroadStagesCheckboxState = JSON.stringify(this.formGroup.get("broadStages")?.value?.sort()) == JSON.stringify(this.globalFilterList?.broadStages?.sort());
  }

  togglePrTypes() {
    this.toggleAllPrTypesCheckboxState = JSON.stringify(this.formGroup.get("prTypes")?.value?.sort()) == JSON.stringify(this.globalFilterList?.prTypes?.sort());
  }

  togglePrAgingBuckets() {
    this.toggleAllPrAgingBucketsCheckboxState = JSON.stringify(this.formGroup.get("prAgingBuckets")?.value?.sort()) == JSON.stringify(this.globalFilterList?.prAgingBuckets?.sort());
  }

  toggleSourcer1() {
    this.toggleAllSourcer1CheckboxState = JSON.stringify(this.formGroup.get("sourcer1")?.value?.sort()) == JSON.stringify(this.globalFilterList?.sourcer1?.sort());
  }

  toggleSourcer2() {
    this.toggleAllSourcer2CheckboxState = JSON.stringify(this.formGroup.get("sourcer2")?.value?.sort()) == JSON.stringify(this.globalFilterList?.sourcer2?.sort());
  }
}
```

<h2><a href="https://github.com/sanjay9616/Angular/blob/master/README.md"> 🔙 Back</a></h2>
