# hand-tracking-stabilization

## Image Stabilization for Hand-tracking Telescope Video
Mark Grandau – Springboard Capstone for ML Engineering

When recording an astronomical observation (comet, planet, star, etc. ) in the sky by hand adjusting (hand-tracking) the telescope; the object being observed is hard to keep consistent in the field of view. This is like using a cell phone to record something in motion. But things in the field of view move in wellknown directions at specific rates based on magnification.

I will investigate image stream stabilization. The goal is to stabilize the image stream in a post processing step. I will attempt to do this by "Transfer Learning". This is the process of using images not necessarily in the domain of the problem under consideration. This approach allows me to overcome the "cold start problem', lack of data. As the application is used more and more data will be gathered to continue to evolve the data set to a more specific domain data set. 
 
There has been work around Machine Learning performing stabilization for handheld cameras, with limited success. My work will specifically investigate a reduced subset of the problem domain. Geometrically the problem domain is where the camera can translate in the x and y coordinates, but the change to the angle of incidence as well as the z (depth) to the camera lens is insignificant.

Simplification of the problem domain, I believe, will allow an existing model may perform better.

The object in the field of view is supposed to be fixed. The problem can reduce to pure observational analysis without identification of a coordinate and application of complicated motion equations based on position in the sky for objects that change position like planets, comets, etc.

Stabilization of the images will help in the process of “stacking” the images to reduce atmospheric results. This stacking is beyond the scope of this investigation but is a potential extension for additional work extending the model or using standard image processing algorithms.

Because if this extension what I want out of the model is a translation vector per frame, not the typical adjusted image, though that will help in quickly analyzing the performance of the model.

## Setup

Current assumptions about using notebooks:

* The notebooks each load any additional modules that may needed beyond the base modules
* They define a SageMaker Studio machine type and environment

## References

Papers:
* "Deep Online Video Stabilization" https://arxiv.org/pdf/1802.08091.pdf

* "A Dataset and Evaluation Framework for Deep Learning Based Video Stabilization Systems" https://ieeexplore.ieee.org/document/8966057, https://madat-machine-learning-data.s3.us-west-2.amazonaws.com/Mark/capstone-project/A+Dataset+and+Evaluation+Framework+for+Deep+Learning+Based+Video+Stabilization+Systems.pdf (access to the paper is limited for Internal Business Use by copywrite)

* "Deep Iterative Frame Interpolation for Full-frame Video Stabilization" https://arxiv.org/pdf/1909.02641.pdf

* additional readings http://www.arxiv-sanity.com/search?q=video+stabilization

GitHubs:
* deep-online-video-stabalization https://github.com/cxjyxxme/deep-online-video-stabilization
* deep-online-video-stabalization-deploy https://github.com/cxjyxxme/deep-online-video-stabilization-deploy
* DUTCode https://github.com/Annbless/DUTCode

Data Sets:
* "A Dataset and Evaluation Framework for Deep Learning Based Video Stabilization Systems" https://github.com/mariito/DVS_ (only able to get Dataset.tar.gz and Dataset-3.tar.gz )
* "DeepStab" http://cg.cs.tsinghua.edu.cn/download/DeepStab.zip

Pre-Trained Models: 
* "DUTPretrained" https://drive.google.com/drive/folders/15T8Wwf1OL99AKDGTgECzwubwTqbkmGn6
