---
title: Git Rev News Edition 94 (December 28th, 2022)
layout: default
date: 2022-12-28 12:06:51 +0100
author: chriscool
categories: [news]
navbar: false
---

## Git Rev News: Edition 94 (December 28th, 2022)

Welcome to the 94th edition of [Git Rev News](https://git.github.io/rev_news/rev_news/),
a digest of all things Git. For our goals, the archives, the way we work, and how to contribute or to
subscribe, see [the Git Rev News page](https://git.github.io/rev_news/rev_news/) on [git.github.io](http://git.github.io).

This edition covers what happened during the months of November 2022 and December 2022.

## Discussions

<!---
### General
-->

<!---
### Reviews
-->

<!---
### Support
-->

## Developer Spotlight: ZheNing Hu

* Who are you and what do you do?

  My name is ZheNing Hu, and I am a participant in the GSOC 2021
  Git community. Currently I am interning at Alibaba (China).

* What would you name your most important contribution to Git?

  When I used `git shortlog --author="ZheNing Hu"` to look at the patches
  I contributed, I was ashamed to find that my patches are quite small and
  simple, because I'm more of a Git learner right now 😄

  If I had to pick one, I'd say it's adding the `--trailer` option to git commit.
  It is very convenient to add something like "Signed-off-by", "Reviewed-by"
  at the end of the commit message.

* What are you doing on the Git project these days, and why?

  Recently I've been working on [implementing a `--scope` option for `git diff`](https://lore.kernel.org/git/pull.1398.v3.git.1669723221.gitgitgadget@gmail.com/)
  and other Git commands. It tries to limit the scope of the file path to the
  [sparse specification](https://github.com/git/git/blob/7c2ef319c52c4997256f5807564523dfd4acdfc7/Documentation/technical/sparse-checkout.txt#L73).

  The reason I wanted to implement this feature is that I was researching
  how monorepo collaborates and discovered that `git pull` might download
  Git objects outside of the sparse specification. Meanwhile, Elijah Newren
  is contributing [technical documentation of git-sparse-checkout](https://git-scm.com/docs/sparse-checkout)
  [ [source](https://github.com/git/git/blob/7c2ef319c52c4997256f5807564523dfd4acdfc7/Documentation/technical/sparse-checkout.txt) ],
  the article details how other Git commands should properly recognize
  sparse-checkout, and suggests implementing the `--scope` option, which
  I think will solve the problem I encountered above, so I hope to implement it.

  This patch was put on hold by me for a while, as no one seemed to review it.

* If you could get a team of expert developers to work full time on
  something in Git for a full year, what would it be?

  I'd like to have a well-developed concurrency model on the Git server side.
  See ["Question: How to execute git-gc correctly on the git server"](https://lore.kernel.org/git/CAOLTT8Tt3jW2yvm6BRU3yG+EvW1WG9wWFq6PuOcaHNNLQAaGjg@mail.gmail.com/)
  for more details.

* If you could remove something from Git without worrying about
  backwards compatibility, what would it be?

  `git checkout`. It can be used to switch branches or restore working tree files,
  I think two functions are somewhat coupled. I don't know if `git switch` and
  `git restore` would be perfect replacements for it.

* What is your favorite Git-related tool/library, outside of
  Git itself?

  [scalar](https://git-scm.com/docs/scalar). Now I really like to use scalar to
  download Git repositories to save time.

* Do you happen to have any memorable experience w.r.t contributing to
  the Git project? If yes, could you share it with us?

  Mainly during GSOC, my mentor Christian Couder and many people in the Git
  community helped me and I learned how to participate in open source for the
  first time. It was a great experience to be brave and discuss technology with
  people from all over the world.

* What is your toolbox for interacting with the mailing list and for
  development of Git?

  GitGitGadget. It has a clean commit process, and it runs GitHub action to
  help me find out if my patch is buggy before committing to the community.

* What is your advice for people who want to start Git development?
  Where and how should they start?

  1. First become its user
  2. Understand its principles through the documentation
  3. Read the source code to understand the general structure of the project
  4. Understand some sub-modules of the project by solving some problems
  5. Learn from others with an open mind

* If there's one tip you would like to share with other Git
  developers, what would it be?

  Stay curious about technology.


## Releases

+ Git [2.39.0](https://public-inbox.org/git/xmqqlencspnl.fsf@gitster.g/),
[2.38.2](https://public-inbox.org/git/xmqqv8miv7qj.fsf@gitster.g/),
[2.39.0-rc2](https://public-inbox.org/git/xmqq7cz59o6y.fsf@gitster.g/),
[2.39.0-rc1](https://public-inbox.org/git/xmqqedtlynq8.fsf@gitster.g/)
+ Git for Windows [2.39.0(2)](https://github.com/git-for-windows/git/releases/tag/v2.39.0.windows.2),
[2.39.0(1)](https://github.com/git-for-windows/git/releases/tag/v2.39.0.windows.1),
[2.39.0-rc2(1)](https://github.com/git-for-windows/git/releases/tag/v2.39.0-rc2.windows.1),
[2.39.0-rc1(1)](https://github.com/git-for-windows/git/releases/tag/v2.39.0-rc1.windows.1)
+ GitHub Enterprise [3.7.2](https://help.github.com/enterprise-server@3.7/admin/release-notes#3.7.2),
[3.6.5](https://help.github.com/enterprise-server@3.6/admin/release-notes#3.6.5),
[3.5.9](https://help.github.com/enterprise-server@3.5/admin/release-notes#3.5.9),
[3.4.12](https://help.github.com/enterprise-server@3.4/admin/release-notes#3.4.12),
[3.3.17](https://help.github.com/enterprise-server@3.3/admin/release-notes#3.3.17)
+ GitLab [15.7](https://about.gitlab.com/releases/2022/12/22/gitlab-15-7-released/)
[15.6.3](https://about.gitlab.com/releases/2022/12/16/gitlab-15-6-3-released/),
[15.5.6](https://about.gitlab.com/releases/2022/12/08/gitlab-15-5-6-released/),
[15.6.2](https://about.gitlab.com/releases/2022/12/02/gitlab-15-6-2-released/),
[15.6.1, 15.5.5 and 15.4.6](https://about.gitlab.com/releases/2022/11/30/security-release-gitlab-15-6-1-released/)
+ GitKraken [9.0.0](https://help.gitkraken.com/gitkraken-client/current/)
+ Sourcetree [4.2.1](https://product-downloads.atlassian.com/software/sourcetree/ReleaseNotes/Sourcetree_4.2.1.html)
+ git-assembler [1.3](https://lore.kernel.org/git/87tu2927yt.fsf@wavexx.thregr.org/)


## Other News

__Various__

* [Highlights from Git 2.39](https://github.blog/2022-12-12-highlights-from-git-2-39/)
  by Taylor Blau on GitHub Blog.
* [Andrew Morton's first pull request](https://lwn.net/Articles/895689/)
  by Jonathan Corbet on LWN\.net (from May 2022).
    * [Git Rev News: Edition 14 (April 20th, 2016)](https://git.github.io/rev_news/2016/04/20/edition-14/)
      mentions, when describing discussions at the Git Contributor Summit
      (part 1, about big repos and big files), that Andrew Morton uses (used?)
      [quilt](https://savannah.nongnu.org/projects/quilt)
      to maintain his "-mm" kernels, and that he sent patches by email.


__Light reading__

* [Billions of unnecessary files in GitHub](https://dev.to/szabgab/billions-of-unnecessary-files-in-github-i85)
  and Git repositories in general, due to missing or lacking
  [`.gitignore`](https://git-scm.com/docs/gitignore)
  files.  Article by Gabor Szabo on DEV\.to (also known as The Practical Dev).
  There is also some good information in comments.
* [What are your git aliases?](https://dev.to/imjoseangel/what-are-your-git-aliases-43om)
  by Jose Angel Munoz on DEV\.to.
* [How to Close a Pull Request - Merge Commit vs Squash vs Rebase on GitHub](https://leonardomontini.dev/close-pr-strategy-merge-commit-squash-rebase/)
  by Leonardo Montini.
* [What is GitOps?](https://about.gitlab.com/topics/gitops/) on GitLab.
    * The topic of GitOps was mentioned in [Git Rev News Edition #42](https://git.github.io/rev_news/2018/08/22/edition-42/),
      [#43](https://git.github.io/rev_news/2018/09/19/edition-43/),
      [#61](https://git.github.io/rev_news/2020/03/25/edition-61/),
      [#62](https://git.github.io/rev_news/2020/04/23/edition-62/),
      and [#89](https://git.github.io/rev_news/2022/07/31/edition-89/)
* [GitOps viewed as part of the Ops evolution](https://about.gitlab.com/blog/2021/07/12/gitops-as-the-evolution-of-operations/)
  by Viktor Nagy o GitLab Blog (2021).
* [A meta talk about Git strategies](https://dev.to/mortenolsen/deployment-confidence-with-git-4b0b)
  for deployment (GitOps-like), by Morten Olsen on DEV\.to.
* [Rebases in Git and why you shouldn't be afraid of them](https://how-to.dev/rebases-in-git-and-why-you-shouldnt-be-afraid-of-them)
  by Marcin Wosinek for [How to dev](https://how-to.dev/)
  (also [reposted on DEV\.to](https://dev.to/how-to-dev/rebases-in-git-and-why-you-shouldnt-be-afraid-of-them-1fb5)).
* [Take advantage of Git rebase](https://about.gitlab.com/blog/2022/10/06/take-advantage-of-git-rebase/)
  by Christian Couder on GitLab Blog.
* [Split a commit into 2 commits with `git rebase`](https://dev.to/thelarkinn/split-a-commit-into-2-commits-with-git-rebase-31ee)
  by Sean Larkin on DEV\.to.
* [Minimum Viable Git for Trunk-based Development](https://blog.trunk.io/minimum-viable-git-for-trunk-based-development-81a5da7a77a7)
  by Eli Schleifer on [trunk.io](https://trunk.io/) blog (a Medium-based blog).
    * [Trunk Based Development](https://trunkbaseddevelopment.com/)
      was mentioned directly in [Git Rev News Edition #24](https://git.github.io/rev_news/2017/02/22/edition-24/)
      and [#73](https://git.github.io/rev_news/2021/03/27/edition-73/).
    * [Patterns for Managing Source Code Branches](https://martinfowler.com/articles/branching-patterns.html)
      by Martin Fowler, mentioned in [Git Rev News Edition #63](https://git.github.io/rev_news/2020/05/28/edition-63/),
      describes Trunk-Based Development in the section
      [Looking at some branching policies](https://martinfowler.com/articles/branching-patterns.html#LookingAtSomeBranchingPolicies).
* [Benefits of Using Pull Requests for Collaboration and Code Review](https://developer.nvidia.com/blog/benefits-of-using-pull-requests-for-collaboration-and-code-review/)
  by Fatos Morina on NVIDIA Developer Technical Blog.
* [How to revert a merge commit then merge again](https://dev.indooroutdoor.io/how-to-revert-a-merge-commit-and-then-merge-again)
  by Jb Rocher on his blog
  ([also on DEV\.to](https://dev.to/jbrocher/how-to-revert-a-merge-commit-then-merge-again-hoo)).
* [Git worktree](https://github.polettix.it/ETOOBUSY/2022/11/22/git-worktree/)
  by Flavio Poletti (@polettix) on his ETOOBUSY blog.
* [Git Notes: Git's Coolest, Most Unloved Feature](https://tylercipriani.com/blog/2022/11/19/git-notes-gits-coolest-most-unloved-feature/)
  by Tyler Cipriani on his blog.
    * You can find various uses of _git notes_ feature mentioned in Git Rev News:
      [marking test suite successes](http://who-t.blogspot.de/2015/07/using-git-notes-for-marking-test-suite.html)
      in [#6](https://git.github.io/rev_news/2015/08/05/edition-6/),
      and [maintaining a high quality change log](https://harrow.io/blog/effortlessly-maintain-a-high-quality-change-log-with-little-known-git-tricks/)
      in [#34](https://git.github.io/rev_news/2017/12/20/edition-34/).
    * [git-appraise](https://github.com/google/git-appraise),
      a distributed code review system for Git repos using git notes
      was mentioned in [Git Rev News Edition #11](https://git.github.io/rev_news/2016/01/13/edition-11/).
* [Learn Git: 3 commands to level up your skill](https://opensource.com/article/22/11/advanced-git-commands)
  by Dwayne McDaniel on Opensource\.com.
* [Code version best practices with clean commit formats](https://blogs.halodoc.io/code-version-best-practices-with-clean-commit-formats/),
  following [angular commit convention guidelines](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#commit),
  by Chaitanya S. on Halodoc blog.
    * [Conventional Commit specification](https://www.conventionalcommits.org/)
      was first mentioned in [Git Rev News Edition #52](https://git.github.io/rev_news/2019/06/28/edition-52/).
    * [commitlint](https://commitlint.js.org/#/) was first mentioned
      in [Git Rev News Edition #81](https://git.github.io/rev_news/2021/11/29/edition-81/),
      [Commitizen](http://commitizen.github.io/cz-cli/)
      in [#72](https://git.github.io/rev_news/2021/02/27/edition-72/),
      [Husky](https://github.com/typicode/husky)
      in [#63](https://git.github.io/rev_news/2020/05/28/edition-63/),
      and [conventional-changelog](https://github.com/conventional-changelog/conventional-changelog)
      in [#81](https://git.github.io/rev_news/2021/11/29/edition-81/).
* [Resolving Merge Conflicts with Visual Studio Code](https://leonardomontini.dev/merge-conflict-vscode/)
  by Leonardo Montini (also [on This is Learning DEV\.to blog](https://dev.to/this-is-learning/resolving-merge-conflicts-with-visual-studio-code-1mn1)).
<!-- this is humor, and should be last entry -->
* [Extremely Linear Git History](https://westling.dev/b/extremely-linear-git),
  where first commit in a repo hash a hash that starts with `0000000`,
  the second commit is `0000001`, the third is `0000002`, and so on
  is possible with [extremely-linear](https://github.com/zegl/extremely-linear)
  (aka `git linearize`) tool.  Article and tool by Gustav Westling.  ☺
    * [Git Rev News Edition #24](https://git.github.io/rev_news/2017/02/22/edition-24/)
      mentions in passing the <s>[git-sham](https://bitbucket.org/tpettersen/git-sham)</s> tool,
      with which you can make it so that subsequent commits have SHA-1 identifiers
      beginning with subsequent numbers - but the tool no longer exists at provided URL.


<!---
__Easy watching__
-->

__Git tools and sites__

* [git-credential-oauth](https://github.com/hickford/git-credential-oauth)
  is a Git credential helper that securely authenticates to GitHub,
  GitLab, BitBucket and other forges using OAuth.
* [semantic-release](https://github.com/semantic-release/semantic-release)
  ([documentation](https://semantic-release.gitbook.io/semantic-release/))
  is a fully automated version management and package publishing Node\.js tool.
* [Release Please](https://github.com/googleapis/release-please) is a Node\.js too that
  automates CHANGELOG generation, the creation of GitHub releases,
  and version bumps for your projects; it does so by parsing your git history,
  and looking for [Conventional Commit](https://www.conventionalcommits.org/) messages
* [gitignore.io](https://www.toptal.com/developers/gitignore/) by Toptal
  is a service that creates useful `.gitignore` files for your project.
    * [github/gitignore](https://github.com/github/gitignore)
      is GitHub's collection of `.gitignore` file templates.
    * Atlassian's Bitbucket has [`.gitignore` Tutorial](https://www.atlassian.com/git/tutorials/saving-changes/gitignor)
    * GitLab provides [.gitignore API](https://docs.gitlab.com/ee/api/templates/gitignores.html)
      for all tiers.
    * [gig](https://github.com/hackrslab/gig),
      a Node\.js command-line tool for quickly setting up `.gitignore` files,
      which uses GitHub's gitignore repository for gitignore templates,
      was mentioned in [Git Rev News Edition #6](https://git.github.io/rev_news/2015/08/05/edition-6/).
    * [.gitignore Generator](https://marketplace.visualstudio.com/items?itemName=piotrpalarz.vscode-gitignore-generator)
      extension for _Visual Studio Code_, which uses the gitignore.io API,
      was mentioned in [Git Rev News Edition #57](https://git.github.io/rev_news/2019/11/20/edition-57/).
* [Diffchecker.com](https://www.diffchecker.com/) is an online service that
  will compare text to find the difference between two text files; there is also
  an option for comparing [images](https://www.diffchecker.com/image-compare/),
  [PDFs](https://www.diffchecker.com/pdf-compare/),
  and [spreadsheets](https://www.diffchecker.com/excel-compare/) in xls/xlsx/xlsm/xlsb, csv, txt, dif, ods formats.
  There is also paid Diffchecker Pro and Diffchecker Desktop app.
* [OpenGitOps](https://opengitops.dev/) is a set of open-source standards,
  best practices, and community-focused education to help organizations
  adopt a structured, standardized approach to implementing GitOps.
    * [GitOps.tech](https://www.gitops.tech/), a similar site that aggregates the essence of GitOps
      (and includes free [GitOps: Cloud-native Continuous Deployment](https://leanpub.com/gitops)
      e-book, published via Leanpub), was mentioned in passing in
      [Git Rev News Edition #62](https://git.github.io/rev_news/2020/04/23/edition-62/).
* [Semantic Versioning Specification (SemVer)](https://semver.org/)
  is a simple set of rules and requirements that dictate
  how version numbers are assigned and incremented.


## Credits

This edition of Git Rev News was curated by
Christian Couder &lt;<christian.couder@gmail.com>&gt;,
Jakub Narębski &lt;<jnareb@gmail.com>&gt;,
Markus Jansen &lt;<mja@jansen-preisler.de>&gt; and
Kaartic Sivaraam &lt;<kaartic.sivaraam@gmail.com>&gt;
with help from ZheNing Hu and Mirth Hickford.