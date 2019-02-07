# General idea

Elevator pitch:

A real life hardware easy-button to create a server
in the cloud, with cost efficiency and security in mind.

3 steps:

1. Deploy the infrastructure (no server)
2. Create and start a server we can log into LIVE
3. Stop/destroy server (to avoid costs)

Caveats

Stopped servers still cost money (ebs storage)
We dont want to destroy all the infra live on stage

The secret?

We will use TF variables, and ternary expressions to
calculate "create 1, or destroy 1" `count` expressions
in terraform

Therefore we never run `tf destroy`, we only ever run `apply` with force true, to alter the resources, even though the result is a destructive action.

How it works?

Streamdeck mini

Set of scripts that do things

Docker containers that do things

Terraform declarations that result in infra

Scripts that report back results

deployment folder:

Terraform scripts

docker folder:

For the presentation

presentation folder:

resources for `mdx-deck`

docs folder for ... does what it says on the tin

scripts folder

What the streamdeck actions actually run
