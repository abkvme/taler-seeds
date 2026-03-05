# taler-seeds

Community-maintained list of [Taler](https://taler.tech) bootstrap nodes.

Taler nodes fetch this list on startup to supplement hardcoded seed addresses, improving network connectivity and decentralization.

## Format

`bootstrap.json` contains a list of nodes. The `host` field can be either a DNS name or an IP address.

```json
{
  "nodes": [
    {"host": "example.com", "port": 23153},
    {"host": "93.125.84.156", "port": 23153}
  ]
}
```

## How to Add Your Node

To add your node to the bootstrap list, follow these steps:

### 1. Fork the Repository

- Go to [https://github.com/abkvme/taler-seeds](https://github.com/abkvme/taler-seeds)
- Click the **Fork** button in the top-right corner
- This creates a copy of the repository under your GitHub account

### 2. Clone Your Fork

```bash
git clone https://github.com/YOUR_USERNAME/taler-seeds.git
cd taler-seeds
```

### 3. Create a Branch

```bash
git checkout -b add-my-node
```

### 4. Edit bootstrap.json

Add your node entry to the `nodes` array in `bootstrap.json`. Make sure your node is running Taler with port 23153 open and reachable.

### 5. Commit and Push

```bash
git add bootstrap.json
git commit -m "Add my node to bootstrap list"
git push origin add-my-node
```

### 6. Create a Pull Request

- Go to your fork on GitHub: `https://github.com/YOUR_USERNAME/taler-seeds`
- Click **Compare & pull request**
- Verify the base repository is `abkvme/taler-seeds` and base branch is `main`
- Add a brief description of your node (location, uptime, etc.)
- Click **Create pull request**

### Requirements

- Your node must be running Taler on port 23153
- The port must be open and reachable from the internet
- Your node should have reliable uptime
