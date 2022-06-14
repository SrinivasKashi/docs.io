#Design Considerations

 
###For designing CI/CD using GitHub Actions we need to consider the standard used in the industry.

##For Pull Request workflow design , consider below points

- Use pull_request_target workflow trigger rsther then pull_request workflow
- Use trigger workflow_run for PR decoration. e.g. https://securitylab.github.com/research/github-actions-preventing-pwn-requests/ 
- Add a condition to the pull_request_target to run only if a certain label is assigned the PR, like safe to test that indicates the PR has been vetted by someone with write privileges to the target repository

##For checkout Stage :
- For actions/checkout pass the optional parameter persist-credentials as false.
- 
  


### References
1. https://securitylab.github.com/research/github-actions-untrusted-input/
2. https://securitylab.github.com/research/github-actions-preventing-pwn-requests/
3. https://securitylab.github.com/research/github-actions-building-blocks/

