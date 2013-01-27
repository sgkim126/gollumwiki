# find

        Model.find(id)
        Model.find(:all)
        Model.find(:all, :conditions => ["field1=? and field2 is ? and field3 in ?", value, nil, list])
        Model.find(:all, :conditions => { :field1 => value, :field2 => nil, :field3 => list})
        Model.find_all_by_field1(value)
        Model.find(:all, :order => 'fieldname DESC')

## collect shorthand
        find(:all).collect{ |p| p.field}

        find(:all).collect(&:field)

### each?

        find(:all).each?(&:field)

### all?

        find(:all).all?(&:field)

### any?

        find(:all).any?(&:field)
