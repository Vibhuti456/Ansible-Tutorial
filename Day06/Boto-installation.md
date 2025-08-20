#### Use a Virtual Environment

```
# Install venv if not already installed
sudo apt install python3-venv -y

# Create a virtual environment
python3 -m venv myenv

# Activate it
source myenv/bin/activate

# Install boto3 inside the venv
pip install boto3

```
##### Deactivate when done:
```
deactivate
```
