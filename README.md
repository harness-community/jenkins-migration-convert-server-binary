
# Jenkins Migration Convert Server

The `jenkins-migration-convert-server` is a lightweight Go tool used by the (Jenkins Migration Plugin)[https://github.com/harness-community/jenkins-migration-convert-server-binary] to convert traces into Harness Pipeline YAML. It must run on the same Jenkins instance as the plugin for YAML conversion to work.

---


## Run

```bash
./convert_server_amd64
```

## Installation Steps

1. **Install the Jenkins Migration Plugin:**
   - Download the latest release from the plugin repository.
   - Deploy the `.hpi` file in Jenkins as per the plugin instructions.

2. **Install the `jenkins-migration-convert-server`:**
   - Clone the server repository.
   - Build the tool using the provided build command.
   - Run the tool on the same machine as Jenkins: using the appropriate binary for your Jenkins environment:
       - `./convert_server_amd64` for amd64 machines
       - `./convert_server_arm64` for arm64 machines

3. **Verify Setup:**
   - Use the Jenkins Migration Plugin to view pipeline YAML. The plugin will send the relevant traces to the server running inside ths tool, which handles the conversion process.
