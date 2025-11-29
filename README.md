# GitHubActions_Demo4.1_Upload_Artifact

Practiced code as below formats::
Format 1:            # It will automatically trigger action when it detects any changes and will push to the master branch
      on: 
       push:
        branches: main

Format 2:            # It will create "Run workflow" button for that workflow
      on: workflow_dispatch    


Practice with below,

      - name: Upload the file to Github Repo as Artifact
        uses: actions/upload-artifact@v4
        with: 
         name: GHA_Artifact
         path: |
          GHA_Artifact_Dir/                             # Upload the entire directory
          # GHA_Artifact_Dir/test.json                  # Or you can specify a single file to upload
          # !GHA_Artifact_Dir/secret_dont_upload.txt    # Exclude specific file from upload
