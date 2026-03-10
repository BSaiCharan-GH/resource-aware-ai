PROJECT ROADMAP

Phase 1 — Setup 

 Set up conda environment
 
 Install all dependencies
 
 Verify CUDA and GPU

Phase 2 — Data

 Download CIFAR-10
 
 Write data loader
 
 Verify dataset loads correctly
 
 Test sample batch visualization

Phase 3 — Model

 Implement base ViT using timm
 
 Test base ViT forward pass on CIFAR-10
 
 Implement early exit heads at layers 4 and 6
 
 Implement multi-exit forward pass
 
 Verify all three exit points produce correct output shapes

Phase 4 — Resource Monitoring

 Implement resource monitor (GPU memory, CPU usage, latency)
 
 Implement resource history buffer
 
 Implement resource drift computation
 
 Test monitor on all three machines

Phase 5 — Decision Controller

 Implement confidence drift detection across exit points
 
 Implement basic controller (confidence + resources)
 
 Extend controller with resource drift signal
 
 Extend controller with confidence drift signal
 
 Test controller logic with dummy inputs

Phase 6 — Training

 Write training loop
 
 Train model on Machine 1 (6GB GPU)
 
 Validate accuracy at each exit point
 
 Save trained model checkpoints

Phase 7 — Experiments

 Run full model inference on all three machines
 
 Run adaptive model inference on all three machines
 
 Record accuracy, latency, GPU memory per exit point
 
 Compare full model vs adaptive model results

Phase 8 — Analysis

 Plot accuracy vs latency trade-offs
 
 Plot resource drift over sustained inference sessions
 
 Plot confidence drift patterns per class
 
 Write up findings

Phase 9 — Documentation

 Update README with final results
 
 Write abstract and novel contributions section
 
 Prepare demo for presentation
 
 Final code cleanup and comments

Phase 10: PUBLISHING PAPER 

