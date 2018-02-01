# Simple form demo
## Features
- Single line helper method for label, input and wrapper
- Options for each with input_helper, label_helper and wrapper_helper
- Validations, placeholder, hint, error message options

## Form vs Simple form

### Form

```
<div class="field">
  <%= f.label "Your name" %>
  <%= f.text_field :name %>
</div>

<div class="field">
  <%= f.label :description %>
  <%= f.text_area :description %>
</div>

<div class="field">
  <%= f.label :active %>
  <%= f.check_box :active %>
</div>
```

### Simple form

```
<%= f.input :name, label: "Your name", error: "Name is mandatory", placeholder: "Your name goes here", 
                    input_html: { class: "form_name" }, 
                    wrapper_html: { class: 'field' } %>

<%= f.input :description, type: :text, wrapper_html: { class: 'field' } %>

<%= f.input :active, type: :check_box, inline_label: "Active", wrapper_html: { class: 'field' } %>
```
