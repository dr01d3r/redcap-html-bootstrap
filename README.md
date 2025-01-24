# redcap-html-bootstrap
A simple repo for distributing Bootstrap-based HTML templates for use within REDCap

> **NOTE:** This is very much a work-in-progress! The inital goal is to get a version of the full conference dashboard HTML out here, which you can find at the link below!
> 
> [Conference Dashboard HTML](/dashboards/conference_full.html)

## Intro

Building a nice looking project dashboard in REDCap can be a lot easier than you might think.  Once you understand the basic concepts of Bootstrap, and a little bit of HTML, you can create beautifully looking experiences for your users!

## Resources

The following resources are already included in REDCap, so they're immediately available without any extra setup necessary.

- Bootstrap ([link](https://getbootstrap.com/docs/5.3/getting-started/introduction/))
  - The frontend toolkit used by REDCap for designing the layout and styling the UI
  - REDCap uses a specific version of Bootstrap.  Most of the time, it is either using the latest or close to the latest version; however, if you find that a css class or component doesn't behave as you expect, it could be due to a version issue.  There are ways to identify which version of Bootstrap your version of REDCap uses, but the easiest solution might just be to ask on Community.
  - The latest supported version as of this writing is `v5.3.3`
- FontAwesome ([link](https://fontawesome.com/search?ic=free))
  - Everything is better with icons!
  - As with Bootstrap, this is also versioned. At the time of writing this guide, the latest supported version was `v6.7.2`, which is currently the latest.

So whenever you're trying to customize some HTML, keep these documentation sites readily available.  I almost always have one or both of these sites open while I build things, either looking for ideas, or grabbing html templates to try something out.

## Layout Design

Building the layout comes down to two primary methods, both heavily documented in the Bootstrap website:

- Grid Layout
- Flex

I won't be able to do this section justice in just a few sentences/paragraphs.  It would be best to read through the docs, do your best to understand it if only just a little bit, and just try them out, play with them in a test project or non-public dashboard.

What I can say with certainty, is that both options are very useful, and often, I find myself combining the two to fine-tune some more tricky layouts that I'm trying to achieve.

## Components

I won't need to provide a lot of HTML here on a per-component basis; however, I will mention the most commonly used components I use in REDCap, a link to their documentation, and any helpful information that you may want/need.

- Cards
- Alerts
- Buttons
- Modal
- Popover/Tooltip

### Card
https://getbootstrap.com/docs/5.3/components/card/

This is a great way to organize content, whether you want many of them, or just one.  They can be used in tons of ways, and can be as simple or as complex as you need them to be.

**Simple Example**

```html
<div class="card">
    <div class="card-header text-center">
        <h4 class="my-0">Conference Agenda</h4>
    </div>
    <div class="card-body lead">
        <div class="mb-3">REDCapCon will bring together REDCap professionals over this 3 &amp; 1/2 day event.</div>
        <div class="mb-3">View the agenda here.</div>
        <a class="btn btn-primary text-light text-decoration-none w-100" href="#" target="_blank" rel="noopener">Go To Dashboard</a></div>
    </div>
</div>
```

![image](https://github.com/user-attachments/assets/7ad73eb5-d60e-45ac-b404-e9f721519e96)

**Complex Example**

> **NOTE:** This has some extra functionality within it (i.e. Modal Dialogs) and won't work without the rest of that HTML.  The intent of this example is to show how complex you can get with it.

```html
<div class="card border align-self-stretch flex-grow-1 mb-3"
     style="border-color: var(--bs-purple) !important;"
>
    <div class="card-header text-white py-3 text-center fw-normal"
         style="background-color: var(--bs-purple) !important;"
    >
        <h4 class="my-0">Complex Card with Custom Coloring and Content</h4>
        <h6 class="my-0">Some Kind of Sub-Header Content</h6>
        <h6 class="my-0">Additional Information</h6>
    </div>
    <div class="alert alert-secondary rounded-0 m-0 p-2 text-center"><i class="fas fa-exclamation-triangle">&nbsp;</i> Special Alert Information Can Go Here! <i class="fas fa-exclamation-triangle">&nbsp;</i></div>
    <div class="card-body d-flex flex-column">
        <div class="row row-cols-lg-4 row-cols-md-3 row-cols-sm-2 ps-3 my-3">
            <ul class="list-bulleted mb-0"><li>Free Airport Transportation</li></ul>
            <ul class="list-bulleted mb-0"><li>Complimentary Breakfast</li></ul>
            <ul class="list-bulleted mb-0"><li>Indoor-Outdoor Whirlpool/Hot tub</li></ul>
            <ul class="list-bulleted mb-0"><li>Fitness Center</li></ul>
            <ul class="list-bulleted mb-0"><li>Indoor Heated Pool</li></ul>
            <ul class="list-bulleted mb-0"><li>Lounge/Bar</li></ul>
            <ul class="list-bulleted mb-0"><li>Restaurant</li></ul>
        </div>
        <div>
            <hr class="mb-2" />
            <div class="text-center fs-6 fw-light">Reservations</div>
            <div class="row text-center fw-bold g-2">
                <div class="col">
                    <div class="mb-2">Pre-Conference Night</div>
                    <a class="btn btn-outline-secondary text-decoration-none w-100" href="#" target="_blank" rel="noopener noreferrer">Sept 13<sup>th</sup> Booking</a>
                </div>
                <div class="col-2">
                    <div class="mb-2">&nbsp;</div>
                    <button class="btn btn-outline-secondary w-100 w-100" type="button" data-bs-toggle="modal" data-bs-target="#call-in-countryinnmn"> <i class="fas fa-phone">&nbsp;</i> </button>
                </div>
                <div class="col">
                    <div class="mb-2">Post-Conference Night</div>
                    <a class="btn btn-outline-secondary text-decoration-none w-100" href="3" target="_blank" rel="noopener noreferrer">Sept 17<sup>th</sup> Booking</a>
                </div>
            </div>
        </div>
    </div>
</div>
```

![image](https://github.com/user-attachments/assets/633fa561-f4ad-4ac6-9df6-983960325148)

### Example Dashboard
![image](https://github.com/user-attachments/assets/6e287ad6-ab47-432b-9f6e-4be38eb189cc)
