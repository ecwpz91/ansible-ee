# Install ansible-builder
python -m pip install --upgrade --user ansible-builder

# Set up content collections
mv ansible.cfg.example ansible.cfg

# Create the project
ansible-builder create

# Build the project
ansible-builder build
