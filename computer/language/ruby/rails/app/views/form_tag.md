# form_tag

        <%= form_tag do %>
            contents
        <% end %>

## ex

        <%= form_tag(some_path, :method=>"get") do %>
            contents
        <% end %>

        <form action="/some" method="get">
            contents
        </form>
