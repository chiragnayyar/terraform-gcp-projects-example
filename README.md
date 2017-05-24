# Terraform GCP Projects Example

This repository contains sample code for using Terraform and Google Cloud
platform to create ephemeral project environments for trainees. The premise is
that each attendee (trainee) gets full access to a project to launch/manage
their own instances, but the instructor has owner access over all projects.

## Usage

1. Fill out `variables.tf` with your org and billing id or us a
  `terraform.tfvars` file.

1. Add a list of trainees

1. Run `terraform plan` to see the changes

1. Run `terraform apply` to apply them

## Miscellaneous

After creating the projects and resources, you will probably want to find them
in the web UI. Visit https://cloud.google.com and authenticate. In the header,
click the dropdown and choose "View all Projects".

If the user you added was in a GCP organization, choose "No Organization" from
the list. If the user is a standard Gmail account, the project will appear in
the default list.

On the "Compute" section, attendees can click "SSH" on their instance to launch
an in-browser SSH session.
