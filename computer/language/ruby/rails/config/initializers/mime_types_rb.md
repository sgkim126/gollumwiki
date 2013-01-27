#mime_types.rb

        Mime::Type.register_alias "text/html", :iphone

        respond_to do |format|
          format.ics { render :text => post.to_ics, :mime_type => Mime::Type["text/calendar"]  }
        end
