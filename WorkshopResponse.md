# Task 1 

Forked repository and added the repo to Coderabbit. 

* [Pull Request](https://github.com/robertnorrie/help-center/pull/1)
* [CodeRabbit dashboard](https://app.coderabbit.ai/dashboard?var-org_id=d92bfaca-34b0-427b-9304-a7330da9199a&var-repo_name=help-center&var-username=All&var-team=All&var-team_users=All) 

I intentionally copied and pasted the sample text from the document into the new file without any correct formatting. 

CodeRabbit ran on the pull request and detected the missing indentation in the code, and suggested the appropriate fixes to commit to resolve this. 

<img width="899" height="723" alt="Screenshot 2025-10-20 at 16 59 58" src="https://github.com/user-attachments/assets/a071bef7-6be5-4b0c-9535-22414fc16aa5" />

CodeRabbit ran again and updated once I committed those suggested changes onto the pull request branch. 

It gave a summary of the pull request contents in the pull request description. 
It gave a summary of the checks that were required and their status to confirm that the pull request was ok to merge. 

It also gave details of what extra context it used in it’s review, this case Ruff to analyse the formatting.

<img width="371" height="82" alt="Screenshot 2025-10-20 at 09 03 54" src="https://github.com/user-attachments/assets/e13154c7-e2b8-4f65-9e2f-6a3f0efa3868" />



# Task 2

I created pull request here: https://github.com/robertnorrie/help-center/pull/2 
Task Rabbit did not run, as the base branch was not the default branch. 

<img width="794" height="428" alt="Screenshot 2025-10-20 at 15 03 09" src="https://github.com/user-attachments/assets/01ea1364-6c7d-4fce-92e5-1cfac5fb0aa5" />

I was able to manually trigger the review by running `@coderabbitai review` in the pull request. 
<img width="1045" height="478" alt="Screenshot 2025-10-20 at 17 00 49" src="https://github.com/user-attachments/assets/3be811d0-ad54-4167-97cf-3697936594e9" />

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

# Task 3

General feedback: 

I found it really straightforward to create an account and authorise access to my repositories and get a review to trigger. 
I had no issues with the initial configuration - I also found the docs really straightforward to search. 

I also really like how configurable the reviews are, especially by being able to configure a yaml file for the configuration. You could add this file to your repo template to ensure it is present for all new repos to ensure consistent experience across repos. 
