# Gensyn-restart-Commands
      
cd rl-swarm

python3 -m venv .venv
. .venv/bin/activate

allocating 24GB Ram

sudo swapoff /dev/sdb

sudo rm -f /swapfile                        # Remove old swapfile if it exists
sudo fallocate -l 24G /swapfile             # Or use dd if fallocate fails
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile

swapon --show

./run_rl_swarm.sh

cc
