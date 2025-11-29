# GitHubActions_Demo4.1_Upload_Artifact

Practice with below,
      - name: Upload the file to Github Repo as Artifact
        uses: actions/upload-artifact@v4
        with: 
         name: GHA_Artifact
         path: |
          GHA_Artifact_Dir/                             # Upload the entire directory
          # GHA_Artifact_Dir/test.json                  # Or you can specify a single file to upload
          # !GHA_Artifact_Dir/secret_dont_upload.txt    # Exclude specific file from upload
