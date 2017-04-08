# Vagrant docker
A vagrant image (ubuntu/trusty64) with docker and docker-compose pre-installed.

## Usage
```ruby
Vagrant.configure(2) do |config|
	config.vm.box = 'AGhost-7/docker'
end
```
