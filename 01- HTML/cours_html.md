# 01- HTML

HTML5 introduces more descriptive HTML tags. These include **main**, **header**, **footer**, **nav**, **video**, **article**, **section** and others.

## Link to Internal Sections of a Page with Anchor Elements

a (anchor) elements can also be used to create internal links to jump to different sections within a webpage.

To create an internal link, you assign a link's href attribute to a hash symbol # plus the value of the id attribute for the element that you want to internally link to, usually further down the page. You then need to add the same id attribute to the element you are linking to. An id is an attribute that uniquely describes an element.

Below is an example of an internal anchor link and its target element:

    <a href="#contacts-header">Contacts</a>
    ...
    <h2 id="contacts-header">Contacts</h2>

When users click the Contacts link, they'll be taken to the section of the webpage with the Contacts header element.

## Nest an Anchor Element within a Paragraph

You can nest links within other text elements.

    <p>
    Here's a <a target="_blank" href="https://www.freecodecamp.org"> link to www.freecodecamp.org</a> for you to follow.
    </p>

Let's break down the example. Normal text is wrapped in the p element:

    <p> Here's a ... for you to follow. </p>

Next is the anchor element <a> (which requires a closing tag </a>):

    <a> ... </a>

target is an anchor tag attribute that specifies where to open the link. The value _blank specifies to open the link in a new tab. The href is an anchor tag attribute that contains the URL address of the link:

    <a href="https://www.freecodecamp.org" target="_blank"> ... </a>

The text, link to www.freecodecamp.org, within the a element is called anchor text, and will display the link to click:

    <a href=" ... " target="...">link to freecodecamp.org</a>

The final output of the example will look like this:

Here's a link to www.freecodecamp.org for you to follow.

## Create a Set of Radio Buttons

You can use radio buttons for questions where you want the user to only give you one answer out of multiple options.

Radio buttons are a type of `input`.

Each of your radio buttons can be nested within its own `label` element. By wrapping an `input` element inside of a `label` element it will automatically associate the radio button `input` with the `label` element surrounding it.

All related radio buttons should have the same `name` attribute to create a radio button group. By creating a radio group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.

Here's an example of a radio button:

    <label> 
    <input type="radio" name="indoor-outdoor">Indoor 
    </label>

It is considered best practice to set a `for` attribute on the `label` element, with a value that matches the value of the `id` attribute of the `input` element. This allows assistive technologies to create a linked relationship between the `label` and the related `input` element. For example:

    <input id="indoor" type="radio" name="indoor-outdoor">
    <label for="indoor">Indoor</label>

We can also nest the `input` element within the `label` tags:

    <label for="indoor"> 
    <input id="indoor" type="radio" name="indoor-outdoor">Indoor 
    </label>

## Create a Set of Checkboxes

Forms commonly use checkboxes for questions that may have more than one answer.

Checkboxes are a type of `input`.

Each of your checkboxes can be nested within its own `label` element. By wrapping an `input` element inside of a `label` element it will automatically associate the checkbox `input` with the `label` element surrounding it.

All related checkbox inputs should have the same `name` attribute.

It is considered best practice to explicitly define the relationship between a checkbox `input` and its corresponding `label` by setting the for attribute on the `label` element to match the id attribute of the associated `input` element.

Here's an example of a checkbox:

    <label for="loving"><input id="loving" type="checkbox" name="personality"> Loving</label>

## Use the value attribute with Radio Buttons and Checkboxes

When a form gets submitted, the data is sent to the server and includes entries for the options selected. Inputs of type `radio` and `checkbox` report their values from the `value` attribute.

For example:

    <label for="indoor">
    <input id="indoor" value="indoor" type="radio" name="indoor-outdoor">Indoor
    </label>
    <label for="outdoor">
    <input id="outdoor" value="outdoor" type="radio" name="indoor-outdoor">Outdoor
    </label>

Here, you have two `radio` inputs. When the user submits the form with the `indoor` option selected, the form data will include the line: `indoor-outdoor=indoor`. This is from the `name` and `value` attributes of the "indoor" input.

If you omit the `value` attribute, the submitted form data uses the default `value`, which is `on`. In this scenario, if the user clicked the "indoor" option and submitted the form, the resulting form data would be `indoor-outdoor=on`, which is not useful. So the `value` attribute needs to be set to something to identify the option.

## Check Radio Buttons and Checkboxes by Default

You can set a checkbox or radio button to be checked by default using the `checked` attribute.

To do this, just add the word `checked` to the inside of an input element. For example:

    <input type="radio" name="test-name" checked>

