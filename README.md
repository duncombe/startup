startup 
=======

Scripts for logging on to a AWS instance and initializing it to play nice
with Coursera's Startup Engineering coursework.

Workflow will be like this: 

1) Open a local terminal window and clone this repositiory to a startup
directory.

2) Populate the configs subdirectory with the secret keys.
	gitconfig: contains the sensitive git configuration information.
	ssh_config: contains the sensitive ssh configuration information.
	github_key.pub, github_key: the keys for accessing github.com.

3) Launch a t1.micro instance from the dashboard at aws.amazon.com running
ubuntu 12.?? server, which will be identified by an <instance_name> of the
form *.compute.amazonaws.com.
	
4) Run start_instance <instance_name>

The start_instance script will log on to the t1.micro instance and git
clone duncombe/dotfiles and duncombe/setup. The setup script in set up will
be run and necessary installations and links will be made. 

You will finally be presented with an interactive shell on the t1.micro
instance.

