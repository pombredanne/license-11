License
----------------

Its lame to go copy and paste license files, so just generate them with short commands.

#### Dependencies
- Ruby
- The gem [thor](https://github.com/wycats/thor)

#### Installation 
Place the .licenses directory in your home directory and the license executable in your PATH.

#### Configuration
Modify the default value on line eight of the license executable to be your name.

```ruby
method_option :name, :type => :array, :aliases => '-n', :default => %w{ YOUR NAME } # <---------
```

#### Usage
```bash
license create mit
```

Or to override the default name

```bash
license create mit -n George Orwell
```

##### Included Licenses

- Apache
- BSD
- GPL
- MIT

#### Adding additional or custom licenses
You can add any additional licenses to be rendered as long as they fulfill these requirements.

1. They must be in the .licenses directory
2. They must have the file extension .erb

To pass the name and year variables into the custom licenses just use standard erb syntax.

As long as these requirements are met the filename will render your custom template.

For example...

```bash
license create custom
```

Will attempt to render .licenses/custom.erb

