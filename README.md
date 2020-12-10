Repro steps:

```bash

# Checkout branch with issue example
git clone https://github.com/heyimalex/react-spring.git
cd react-spring && git checkout issue-example

# Install issue example deps
(cd issue-example && yarn install)

# Build react-spring and run the example, open browser, see no error
(yarn install && cd issue-example && yarn serve)

# Revert hotfix commit
git revert --no-edit 88d26c3f

# Run the example again, open browser console, see error
(yarn install && cd issue-example && yarn serve)

```
