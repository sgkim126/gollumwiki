# asp 페이지에서 server-side script 사용하기.
## In-line statements

        <%@ language="vbscript"%>
        <% if i > 10 then i=0 %>

## In-line expressions

        <%@ language="vbscript"%>
        <%= iff(s=="", "empty", s) %>

## script block

        <script language="vbscript" runat="server">
        if i > 10 then i=0
        </script>
