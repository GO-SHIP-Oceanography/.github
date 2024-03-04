Hi `<Insert Github User>` here is your repository for the `<Insert Code Name>` code!

I have created it with an empty README.md, a .gitignore for `<Insert Language>` code, and an `<Insert License>` License.
I have invited you to be an administrator for this repository.

The first task is an initial upload of the code.
We suggest you do this in a branch so that we can review and tidy things before adding them to main.
Below are instructions for this copied from the [Contribution Guidelines](https://github.com/GO-SHIP-Oceanography/.github/blob/main/contributing.md#adding-code):

Navigate into the folder that contains your code and then run, from the terminal:
```
git init
git remote add origin git@github.com:GO-SHIP-Oceanography/<your-repo-name>.git
git pull origin main
```
to pull any base documents (e.g. license).  

_**Note**: This assumes you are accessing a repository via ssh (advised). If you prefer to
access via https you can use
`git remote add origin https://github.com/GO-SHIP-Oceanography/<your-repo-name>.git`
and will be prompted for your GitHub username and password each time you access._

We suggest that you perform your initial upload from a branch, allowing the code to be
reviewed before it is contributed to the main branch, and checked to ensure that it
works and is reproducible.
To do this run:
```
git checkout -b first-commit
```

Following this you can add files using [`git add`](https://github.com/git-guides/git-add),
commit them using [`git commit`](https://github.com/git-guides/git-commit) and push them
to the repository using [`git push`](https://github.com/git-guides/git-push) as usual.
The [Turing Way guide](https://the-turing-way.netlify.app/reproducible-research/vcs/vcs-git)
is a useful guide for those new to these ideas.

Once you are ready for the initial upload run:
```
git push origin first-commit
```
to upload the code to GitHub.

You can then open a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
from the repository webpage on GitHub to ask to add your code to the main branch.

If you are unsure about any part of this process we are happy to guide you through it.
