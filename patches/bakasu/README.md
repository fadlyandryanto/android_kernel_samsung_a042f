# BakaSU + SusFS patches

Applied by CI when the "Build with BakaSU" input is checked.

Generated from a04e-BakaSU @ 7922429
Base:                  a04e @ a758225

Regenerate:
  git checkout -b tmp-bakasu a04e
  git am patches/bakasu/*.patch     # fix conflicts if any
  git format-patch a04e..tmp-bakasu -o /tmp/out
  cp /tmp/out/*.patch patches/bakasu/
  git checkout a04e
  git branch -D tmp-bakasu
  git add patches/bakasu && git commit