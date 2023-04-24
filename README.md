# Install ansible-builder
python -m pip install --upgrade --user ansible-builder

# Set up content collections
mv ansible.cfg.example ansible.cfg

# Create the project
ansible-builder create

# Build the project
ansible-builder build

# Tag the container
podman tag localhost/ansible-execution-env:latest quay.io/yourusername/ansible-execution-env:latest

# Login to container registry
podman login quay.io

# Push the execution environment
podman push quay.io/yourusername/ansible-execution-env:latest
