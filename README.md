# README

### Autoloading Example

#### FoosController first:

```
Loading development environment (Rails 5.2.0.alpha)
irb(main):001:0> Api::FoosController
=> Api::FoosController
irb(main):002:0> Mixins::B
=> Mixins::B
irb(main):003:0>
```

#### FoosController last:
```
Loading development environment (Rails 5.2.0.alpha)
irb(main):001:0> Mixins::B
=> Mixins::B
irb(main):002:0> Api::FoosController
NameError: uninitialized constant Mixins::A
	from app/controllers/api/foos_controller.rb:3:in `<class:FoosController>'
	from app/controllers/api/foos_controller.rb:2:in `<module:Api>'
	from app/controllers/api/foos_controller.rb:1:in `<top (required)>'
	from (irb):2
irb(main):003:0>
```
