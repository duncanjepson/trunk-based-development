# Releasing

## Create a release from master
```bash
git checkout master && git pull
# bump version & update changelog (manual until automation is added)
git tag -s v3.5.0 -m "Release 3.5.0"
git push origin v3.5.0
# create a GitHub Release and attach notes/artifacts
```

# One-off hotfix
```bash
git checkout v3.5.0
git checkout -b hotfix/3.5/issue-xyz
# implement fix, tests
# open PR -> base: master (CI + review)
git checkout master && git pull
git tag -s v3.5.1 -m "Patch 3.5.1 (issue xyz)"
git push origin v3.5.1
```

# Backport to an LTS line
```bash
git fetch origin
git checkout -b hotfix/2.1/issue-xyz origin/release/2.1
git cherry-pick <sha-from-master>
# open PR -> base: release/2.1 (CI + review)
git checkout release/2.1 && git pull
git tag -s v2.1.2 -m "Security fix xyz"
git push origin v2.1.2
# forward-integrate to master if needed
```