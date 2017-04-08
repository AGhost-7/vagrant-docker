# Vagrant docker
A vagrant image(ubunut/trusty63) with docker and docker-compose pre-installed.

## Usage
```ruby
Vagrantfile.configure(2) do |config|
	config.vm.box = 'aghost7/docker'
end
```
