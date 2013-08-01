# Basic commands

    :Git [args]              # does what you'd expect

all of your `~/.gitconfig` aliases are available.

    :Git! [args]             # same as before, dumping output to a tmp file

Moving inside a repo.

    :Gcd [dir]               # :cd relative to the repository

    :Glcd [dir]              # same as above, local to the current window

# Blame

    :Gblame

- `A` resizes to end of author column
- `C` resizes to end of commit column
- `D` resizes to end of date/time column
- `<CR>` quits blame buffer, then opens commit

# Working with the index

    :Gwrite                  # add

    :Gread                   # checkout

    :Gremove                 # rm

    :Gmove                   # mv

in the `Gmove` context, `/` represents the root of the git repository.

    :Gstatus                 # brace yourselves

     <CR>  |:Gedit|
     <C-n> and  <C-p> for moving around files

     -     |:Git| add        # both work in Visual mode too
     -     |:Git| reset (staged files)

     cc    |:Gcommit|

     D     |:Gdiff|
     ds    |:Gsdiff|
     dp    |:Git!| diff (p for patch; use :Gw to apply)
     dp    |:Git| add --intent-to-add (untracked files)
     dv    |:Gvdiff|

     o     |:Gsplit|

     p     |:Git| add --patch

     q     close status
     R     reload status

# Diffs

    diffget [bufspec]        # `do` can be used instead (*d*iff *o*btain)
    diffput [bufspec]
    diffupdate

`[c` and `]c` for navigating changes.

    diffget //1 | diffupdate # `|` is used to chain operations

# Solving merge conflicts with 2-way diffs

    :Gdiff                   # on the file with the conflict

# Browsing the git object database

    `:Gedit`

can be used to open a _read-only_ buffer with the contents of any git object

## Blobs

    :Gedit branchname:path/to/file
    :Gedit feature:%

## Trees, commits and tags can be browsed too

    :Gedit SHA               # will open a buffer with the git object referenced by `SHA`

# History

## Revisions of a file

    :Glog [args]             # opens a buffer with the revisions of the current file

`:cnext`, `:cprevious`, `:cfirst` and `:clast` can be used to move between revisions

    :Glog -10                # opens only the last 10 revisions

## Commits

    :Glog --                 # load all commits into the quickfix list

    :Glog -- %               # load all commits that affected the current file into the quickfix list

# Searching

## Working copy files

    :Ggrep 'whatever'

## Index

    :Ggrep --cached 'whatever'

## Branches

    :Ggrep whatever branch   # search for `whatever` in `branch`

## Tags

    :Ggrep whatever tagname  # search for `whatever` in tag `tagname`

## Commit messages

    :Glog --grep=whatever -- # search for `whatever` in all commit messages

    :Glog --grep=w00t -- %   # search for `w00t` in all commit messages that touched the current file

## Added or removed words

    :Glog -Swhatever --      # search for `whatever` in the diff for each commit
    :Glog -Swhatever --  %   # search for `whatever` in the diff for each commit that touched the current file

# Status line

    set statusline=%<%f\ %h%m%r%{fugitive#statusline()}%=%-14.(%l,%c%V%)\ %P

# Further information

    :help fugitive

Vimcasts on fugitive.vim

- http://vimcasts.org/episodes/fugitive-vim---a-complement-to-command-line-git/
- http://vimcasts.org/episodes/fugitive-vim-working-with-the-git-index/
- http://vimcasts.org/episodes/fugitive-vim-resolving-merge-conflicts-with-vimdiff/
- http://vimcasts.org/episodes/fugitive-vim-browsing-the-git-object-database/
- http://vimcasts.org/episodes/fugitive-vim-exploring-the-history-of-a-git-repository/

# Related plugins

- vim-gitgutter
- vim-mercenary (`fugitive` port for mercurial)
