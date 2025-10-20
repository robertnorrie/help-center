# Task 1 

Forked repository and added the repo to Coderabbit. 

* Pull Request: https://github.com/robertnorrie/help-center/pull/1
* CodeRabbit dashboard: https://app.coderabbit.ai/dashboard?var-org_id=d92bfaca-34b0-427b-9304-a7330da9199a&var-repo_name=help-center&var-username=All&var-team=All&var-team_users=All 

I intentionally copied and pasted the sample text from the document into the new file without any correct formatting. 

CodeRabbit ran on the pull request and detected the missing indentation in the code, and suggested the appropriate fixes to commit to resolve this. 

CodeRabbit ran again and updated once I committed those suggested changes onto the pull request branch. 

It gave a summary of the pull request contents in the pull request description. 
It gave a summary of the checks that were required and their status to confirm that the pull request was ok to merge. 

It also gave details of what extra context it used in it’s review, this case Ruff to analyse the formatting.



# Task 2

I created pull request here: https://github.com/robertnorrie/help-center/pull/2 
Task Rabbit did not run, as the base branch was not the default branch. 
I was able to manually trigger the review by running `@coderabbitai review` in the pull request. 
I consulted the documentation and noted that additional base branches can be configured for auto reviews, either in the `coderabbit.yaml` file, or in the repository settings in the UI under *review > auto review > ~base branches* 

This is the response I would send to a customer experiencing this issue: 


> Hi there, 
>
> Thanks for reaching out and sharing the link to your pull request. 
> It looks like you are trying to create a PR into a base branch other than your default branch. By default, CodeRabbit only runs when your pull request base branch is your default branch. 
> 
> However you can manually trigger a CodeRabbit review by commenting on the pull request using `@coderabbitai review`
> 
> If you would like CodeRabbit to run automatically on other base branches, you can set these in your coderabbit.yaml file: 
>
> ```
> # Configuration for auto review
>   # Default: {}
>   auto_review:
>     # Base branches (other than the default branch) to review. Accepts regex patterns. Use '.*' to match all branches.
>    # Default: []
>    base_branches: []
> ```
> 
> For more information see: https://docs.coderabbit.ai/reference/configuration#param-base-branches 
> 
> If you haven’t configured a coderabbit.yml file, you can do this by using our template which is here: https://docs.coderabbit.ai/reference/yaml-template 
> 
> Alternatively, you can also set base branches for auto review in the CodeRabbit UI, under your repository settings: 
> https://app.coderabbit.ai/repository/1079665568/settings?tab=review&innerTab=auto_review
> 
> I hope that helps solve your issue - if there is anything else we can help with please let me know. 
> 
> Kind regards, 
> 
> Robert 
