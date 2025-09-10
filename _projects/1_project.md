---
layout: page
title: Computer Vision in Transportation Sector
description: Deep learning models for safety and traffic monitoring applications
img: assets/img/cv_transportation.jpg
importance: 1
category: work
related_publications: true
---

**Bottom Line:** Developed and deployed computer vision models for three critical transportation safety applications: traffic sign detection, human-car detection, and PPE compliance monitoring, achieving high precision.

Computer vision technology has revolutionized transportation safety by enabling automated detection and monitoring systems that can process visual information faster and more consistently than human observers. This project explores three key applications of computer vision in the transportation sector, demonstrating the practical implementation of deep learning models for real-world safety challenges.

## Understanding Computer Vision

Computer vision enables machines to interpret and understand visual information from images, similar to human visual perception but with enhanced consistency and speed. The technology works through pretrained CNN (YOLOv8) that learns to recognize patterns by training on labeled datasets.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/YOLOv8_Architecture.jpg" title="Deep learning architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    YOLOv8 with head, backbone, bottleneck layers to detect personal protective equipment. <a href="https://github.com/ultralytics" target="_blank">Learn more about neural networks</a>.
</div>


## Project Applications

### Traffic Sign Detection

The application focused on automated traffic sign recognition using the German Traffic Sign Detection Benchmark dataset with over 50,000 images. The system can identify and classify various traffic signs including prohibitory signs, danger signs, mandatory signs, and other regulatory signage.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/traffic_signs_dataset.png" title="German traffic signs dataset" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The comprehensive German Traffic Sign Detection Benchmark includes multiple categories of signs critical for autonomous vehicle navigation.
</div>

**Performance Results:**

| Sign Category | Precision | Recall |
|---------------|-----------|---------|
| Prohibitory Signs | 96% | 89% |
| Danger Signs | 93% | 89% |
| Mandatory Signs | 95% | 91% |
| Other Signs | 93% | 82% |

**Key Applications:**
- Autonomous vehicles interpreting road signs for navigation
- Driver assistance systems providing real-time alerts  
- Traffic management systems ensuring road safety compliance
