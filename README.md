License
----------------

Its lame to go copy and paste license files, so just generate them with short commands.

#### Dependencies
- Ruby
- The gem [thor](https://github.com/wycats/thor)

#### Installation 
Place the .licenses directory in your home directory and the license executable in your PATH.

#### Usage
```bash
license create mit
```

Or to override the default name

```bash
license create mit -n George Orwell
```

#### Configure a default name
Modify the default value on line eight of the license executable to be your name.

```ruby
method_option :name, :type => :array, :aliases => '-n', :default => %w{ YOUR NAME } # <---------
```


##### Included Licenses (command in parens)

- Apache v2.0 (apache)
- BSD (bsd)
- GPL (gpl)
- MIT (mit)

#### Adding additional or custom licenses
Adding additional templates is very simple, just add any erb template into
the .licenses directory and you can call create on it by its filename.

For example...

```bash
license create custom
```

Will attempt to render .licenses/custom.erb

