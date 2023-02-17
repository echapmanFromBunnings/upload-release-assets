# upload-release-assets
Action to easily upload release assets to existing release

Action provides ability to update an existing release with more assets

```
- uses: echapmanFromBunnings/upload-release-assets@1.3
  with:
    releaseTag: '1.1.1'
    githubToken: ${{ secrets.GITHUB_TOKEN }}
    files: |
      text1.txt
      text2.txt
      ./buildArtfacts/*
```

Alternatively you can provide an artefact name and it will upload accordingly

```
- uses: echapmanFromBunnings/upload-release-assets@1.3
  with:
    releaseTag: '1.1.1'
    githubToken: ${{ secrets.GITHUB_TOKEN }}
    artefactName: my-artefacts-for-upload
```

There is also an override option available, for if the asset already exists.
This is off by default

```
- uses: echapmanFromBunnings/upload-release-assets@1.3
  with:
    releaseTag: '1.1.1'
    githubToken: ${{ secrets.GITHUB_TOKEN }}
    artefactName: my-artefacts-for-upload
    overrideExistingArtefact: true
```
