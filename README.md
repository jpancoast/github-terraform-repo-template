# github-terraform-repo-template
Github repo template with protections "built in" (pre-commit hooks, github actions, etc.)

# Why this repo
To start off with a sane, safe baseline to prevent a disaster later on, ie, having to remove secrets from the git history, nothing is formatted in a sane manner, code that doesn't pass simple tf validate doesn't get pushed, etc.

## What does this repo do
### pre-commit hooks:
* trufflehog (secret scanning)
* terragrunt hclfmt
* trailing-whitespace
* end-of-file-fixer
* detect-aws-credentials
* check-added-large-files
* tfsec
* terraform validate
* terraform fmt
* terraform docs
* tflint

If you do not want to use any of these pre-commit hooks you can comment them out in the `.pre-commit-config.yaml` file in the root of this repo

### To use this repo:
#### Requirements on the developers machine:
* [pre-commit](https://pre-commit.com/)
* [trufflehog](https://github.com/trufflesecurity/trufflehog)
* [tflint](https://github.com/terraform-linters/tflint)
* [tfsec](https://tfsec.dev)
* [terraform](https://www.terraform.io/)
* [terragrunt](https://terragrunt.gruntwork.io/)

After every fresh clone of the repo, the developer needs to cd into the directory and run `pre-commit install`. We're trying to figure out how to have that run automatically but haven't yet.

#### Branch Protection:
NOTE: Branch protection only works for Github team or enterprise installations, OR Public repos

#### CODEOWNERS
