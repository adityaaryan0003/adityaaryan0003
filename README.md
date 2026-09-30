name: Update Space Shooter Game

on:
  schedule:
    - cron: '0 0 * * *'  # Daily at midnight UTC
  workflow_dispatch:  # Allow manual trigger

permissions:
  contents: write

jobs:
  update-game:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v6
        with:
          fetch-depth: 2  # This is crucial!

      - uses: czl9707/gh-space-shooter@v2
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          output-path: 'game.gif'
          strategy: 'random'
          ![My GitHub Game](game.gif)
          pip install gh-space-shooter
          # Clone the repository
git clone https://github.com/yourusername/gh-space-shooter.git
cd gh-space-shooter

# Install with uv
uv sync

# Or with pip
pip install -e .
