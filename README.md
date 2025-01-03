# Learning-control-from-pixels

Unsupervised methods for pretraining Vision-Language-Action (VLA) models without ground-truth robot action labels. Existing Vision-Language-Action models require action labels typically collected by human teleoperators during pretraining, which significantly limits possible data sources and scale. In this work, we propose a method to learn from internet-scale videos that do not have robot action labels. We first train an action quantization model leveraging VQ-VAE-based objective to learn discrete latent actions between image frames, then pretrain a latent VLA model to predict these latent actions from observations and task descriptions, and finally finetune the VLA on small-scale robot manipulation data to map from latent to robot actions.

*** 

In the community, it has been a long-standing question about whether we can learn a good action policy from RAW video which are way much larger-scale than robotics data. The intuition is simple. In human instructional videos, people have already demonstrated the action sequences to accomplish a wide range of daily tasks, such as cooking a dish, fixing a bicycle, building a lego, replacing a battery, etc. The open question is whether we can squeeze such knowledge from raw observations and embody them into a real robot. 

The answer is Yes! This work demonstrated a great potential of learning robotic manipulation from instructional videos that depict fine-grained actions and dynamics, using a latent pretraining strategy. It is easy to train, scale-up, & allievates the heavy dependence on robotics data collection.
