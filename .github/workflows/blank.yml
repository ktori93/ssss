name: Get Busybox Image
on: 
  workflow_dispatch:

jobs:
  save:
    runs-on: ubuntu-latest
    steps:
      - name: Pull and Save Busybox
        run: |
          docker pull busybox:latest
          docker save -o busybox.tar busybox:latest
      
      - name: Upload Busybox Artifact
        uses: actions/upload-artifact@v4
        with:
          name: busybox-image
          path: busybox.tar
