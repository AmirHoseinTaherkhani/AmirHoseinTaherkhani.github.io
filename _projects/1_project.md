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

### PPE Detection System

The Personal Protective Equipment detection system represents a critical safety application for construction and infrastructure work environments. Using a YOLOv8 architecture, the model identifies whether workers are properly wearing required safety equipment.

**Dataset Overview:**
The system was trained on 3,200 carefully annotated instances:
- Training: 2,991 instances
- Validation: 119 instances  
- Testing: 90 instances
- Detection categories: helmet, no helmet, vest, no-vest, person

### Model Performance Analysis

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ppe_precision_recall_curve.png" title="PPE detection precision-recall curves" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ppe_confusion_matrix.png" title="PPE detection confusion matrix" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Precision-Recall curves for each PPE category showing the trade-off between precision (accuracy of positive predictions) and recall (completeness of positive detection). Higher curves indicate better performance, with the area under each curve representing the average precision score. Right: Normalized confusion matrix displaying classification accuracy between different PPE states, with darker diagonal values indicating correct classifications and off-diagonal values showing misclassification patterns.
</div>

### Detection Results

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ppe_detection_batch.png" title="PPE detection validation batch results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Validation batch demonstrating the model's real-world performance across diverse construction scenarios. Each detection shows bounding boxes with confidence scores, successfully identifying workers and their PPE compliance status including helmet presence/absence and vest visibility. The results showcase the system's ability to handle multiple workers simultaneously, various poses, and different lighting conditions while maintaining high detection accuracy.
</div>

**Critical Applications:**
- Real-time PPE compliance monitoring for construction sites
- Automated safety violation detection and reporting
- Supervisor alert systems for immediate safety intervention
- Regulatory compliance documentation for OSHA requirements
- Data-driven safety training program development

## Technical Implementation and Impact

The YOLOv8-based PPE detection system has been successfully deployed and integrated into construction safety workflows. The model demonstrates robust performance in challenging real-world conditions, providing construction managers with automated tools to maintain consistent safety standards and reduce workplace accidents through proactive monitoring and immediate violation detection.