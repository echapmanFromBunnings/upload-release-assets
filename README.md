# upload-release-assets
Action to easily upload release assets to existing release

Action provides ability to update an existing release with more assets

```
- uses: echapmanFromBunnings/upload-release-assets@v1
  with:
    releaseTag: 'v1.1.1'
    githubToken: ${{ secrets.GITHUB_TOKEN }}
    files: |
      text1.txt
      text2.txt
      ./buildArtfacts/*
```

Alternatively you can provide an artefact name and it will upload accordingly
```
- uses: echapmanFromBunnings/upload-release-assets@v1
  with:
    releaseTag: 'v1.1.1'
    githubToken: ${{ secrets.GITHUB_TOKEN }}
    artefactName: my-artefacts-for-upload
```
