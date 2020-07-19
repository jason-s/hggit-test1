YES it works!!!!!

Now using hg-git as per https://www.mercurial-scm.org/wiki/HgGit

Done once:

- `hg clone https://foss.heptapod.net/mercurial/hg-git ~/.hgext/hg-git`
- `sudo /opt/local/Library/Frameworks/Python.framework/Versions/2.7/bin/easy_install dulwich==0.19.11`
- added to my ~/.hgrc file:

      [extensions]
      hgext.bookmarks = 
      hggit = ~/.hgext/hg-git/hggit
- generated an SSH key in ~/.ssh/SOMEKEYFILE (`ssh-keygen -t rsa -b 4096 -C "my-email@gmail.com" -f ~/.ssh/SOMEKEYFILE`)
- added the SOMEKEYFILE.pub file to my github account


Done for each repo:

- added to my repo's .hg/hgrc file:

      [paths]
       github = git+ssh://git@github.com:jason-s/hggit-test1.git

      [ui]
      ssh = ssh -C -i ~/.ssh/SOMEKEYFILE

