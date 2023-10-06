```bash
echo "deb [trusted=yes] https://github.com/renan028/dubins_curves/raw/focal-noetic/ ./" | sudo tee /etc/apt/sources.list.d/renan028_dubins_curves.list
echo "yaml https://github.com/renan028/dubins_curves/raw/focal-noetic/local.yaml noetic" | sudo tee /etc/ros/rosdep/sources.list.d/1-renan028_dubins_curves.list
```
