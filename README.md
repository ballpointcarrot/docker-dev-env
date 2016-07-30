Docker Development Environment
==============================

I've seen a lot of things on the Internet about "How to launch *x* in Docker," but
I've never seen anything that actually makes *use* of the things that are being launched.

In an effort to change that, I've captured my development environment requirements into
a set of docker containers. This gives me two things:

# I get to see something that's built in Docker that isn't a long-running application, but still serves a useful purpose.
# I get to create a portable development environment for myself, so that all I need is a `docker pull` and I'm in business.

I'm provisioning these containers in Ansible, based on posts that I've read concerning the 
configuration of environments from around the Internet:

[Remote Pairing with Docker](https://www.ctl.io/developers/blog/post/cloud-coding-docker-remote-pairing/)
[Building a "zen" CLI environment](http://www.theodo.fr/blog/2014/01/build-a-zen-command-line-environment-with-git-tmux-oh-my-zsh-mosh-and-docker/)



