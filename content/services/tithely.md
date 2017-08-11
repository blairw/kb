---
Title: tithe.ly
show_in_header_nav: false
---

*&larr; back to [Services](%base_url%/?services)*

# tithe.ly

**[tithe.ly](https://tithe.ly/)** is a payments processing service for churches.

## Giving Types

Payments can be categorised under various **giving types** (functionally, projects). This is super useful since it allows tithe.ly to be a lift-and-shift module for payments processing under a wider crowdfunding platform.

To modify giving types *(assuming you're already logged in)*, go to [My Churches](https://tithe.ly/my-churches) and then **Edit Organization** for the church in question. The giving types are at the bottom, and after adjusting them you can just **Save**.

## Programmatic Access

Under the [Website Giving](https://tithe.ly/website-widget) section, the "Simple Giving Widget" offers a code fragment and advises the following parameters:

> `data-action` : Change the name of the giving button on the form (default is "Give") <br />
> `data-giving-to` : Force the form to a specific giving type (for example, "Conference Fee") <br />
> `data-amount` : Force a specific amount (for example, "150" for $150 or "125.99" for $125.99)

Of all these options, `data-giving-to` is perhaps the most interesting since it allows embedded buttons to target particular projects (again, great for setting up a crowdfunding kind of scenario). It is used like so: a key-value specification like `data-giving-to="Hello Joshua"` is inserted into the code fragment's `<button>` element.

As of time of writing (August 2017), the value is not cross-checked against the Giving Types set up by the admin. The string is received by tithe-ly and recorded in the books as-is.