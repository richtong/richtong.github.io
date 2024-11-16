# Rich Tong's Github Pages

This requires some special setup. Every user or organization gets a free
github.io page, you need create a repo with your organization name in it like
this:

```sh
ORG=richtong
gh repo create --public $ORG/$ORG.github.io

```

This will generate an automatic action to publish at "$ORG.github.io" which is
pretty cool. But unless you pay you can't do this with GitHub Free, you need to
upgrade to at least GitHubPro for $48/year.

## Using Hugo with Github Pages

This is a little tricky, first install the .nojekyll file, then in the Build and
Deployment section source pick GitHub Actions and browse all workflows. You will
find a Hugo action so select it. This adds an action on the main branch of the
github.io repo you just made and makes a hugo site. Pretty neat.

## The vanity stuff with $ORG/$ORG

There is another vanity repo which let's you post cool things in your profile
called just "$ORG".

```sh
ORG=richtong
gh repo create --public $ORG/$ORG
```

This doesn't have the `.github.io` extension

## Using this for mkdocs

[Mkdocs Ghdeploy](https://www.mkdocs.org/user-guide/deploying-your-docs/) has
special code to help you to deploy this to a Project Page or to the User or
Organization Page. And the code is not available yet.

```sh
mkdocs gh-deploy
```

This builds the documents and push it a branch in your proejct page. But you
have to create the Project Page first. You have to go to your public repo you
want to open source and document and look in `_Your repo> > Settings > General>
Code and automation > Pages` and then you can actuall decide if you want
automation so source is `Deploy from a branch`

Then `Branch` set to `gh-pages`. Note that behind the scenes it defaults to
[Jekyll](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
to build sites, so if you want something different, you can use mkdocs
deploy or you can add a `.nojekyll` to prevent it

## To add this to the ./src repo

To recreate this,

```sh
# assuming your src repo is in ~/ws/git/src and WS_DIR is set to the path to it
mkdir -p $WS_DIR/git/src/web
cd $WS_DIR/git/src/web
gh repo create _yourorg_/_thisrepo_ --private
git submodule add git@github.com:_yourorg_/_this repo_
```

Now you add the universal theme module to hugo.yaml
