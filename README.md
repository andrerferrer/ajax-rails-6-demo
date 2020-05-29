
## How to implement ajax for Restaurants

### On create
Add remote true to the form
```erb
<%= simple_form_for([ @restaurant, @review ], remote: true) do |f| %>
  <%= f.input :content %>
  <%= f.button :submit %>
<% end %>
```

### On destroy
implement it on the routes and controller

Add remote true to the form
```erb
<%= link_to "X", restaurant, method: :delete, remote: true %>
```

## Debugging
add the gem
`gem 'turbolinks_render'`

## UJS
```ruby
# config/application.rb
config.action_view.embed_authenticity_token_in_remote_forms = true
```
