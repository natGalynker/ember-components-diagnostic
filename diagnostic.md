# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
  componenets
    years
      months
        componenet.js
        template.hbs
      weeks
        component.js
        template.hbs
    component.js
    template.hbs

    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
ember generate componenet my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
  when creating a component the template.hbs and the component.js are the files which get edited. template.hbs is what hold all the markup, and the componenet.js file is what holds any actions the component will handle. These actions can be anything from CRUS actions to haddling click handlers that will change the css.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
  <h3 class='contact-class'}>{{contact.title}}</h3>
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.phone as |phone|}}
        {{my-phone/my-phone phone=phone}}
      {{/each}
    ```
