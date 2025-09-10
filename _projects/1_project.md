---
layout: page
title: Computer Vision in Transportation Sector
description: Deep learning models for safety and traffic monitoring applications
img: assets/img/cv_transportation.jpg
importance: 1
category: work
related_publications: true
---

**Bottom Line:** Developed and deployed computer vision models for three critical transportation safety applications: traffic sign detection, human-car detection, and PPE compliance monitoring, achieving high precision with real-time inference capabilities.

Computer vision technology is transforming transportation safety by enabling automated detection and monitoring systems that process visual information with superhuman consistency and speed. This project demonstrates the practical implementation of deep learning models for real-world safety challenges, bridging the gap between cutting-edge AI research and industry applications that save lives.

## Interactive PPE Detection Demo

Experience the PPE detection system in action. Upload construction site images to see real-time safety compliance monitoring:

<iframe src="https://amirt-cosmos.hf.space" 
        width="100%" height="600px" 
        frameborder="0"
        loading="lazy"
        sandbox="allow-scripts allow-same-origin">
</iframe>

*Try uploading images of construction workers to see how the AI identifies safety equipment in real-time.*

## Understanding Computer Vision

Computer vision enables machines to interpret and understand visual information from images, mimicking human visual perception while surpassing it in consistency, speed, and endurance. Unlike human observers who may experience fatigue or distraction, AI systems maintain unwavering attention to safety-critical details across thousands of monitoring hours.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/YOLOv8_Architecture.jpg" title="Deep learning architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    YOLOv8 architecture featuring specialized head, backbone, and bottleneck layers optimized for real-time object detection. <a href="https://github.com/ultralytics" target="_blank">Explore the technical implementation</a>.
</div>

## Project Applications

### Traffic Sign Detection: Enabling Autonomous Navigation

Automated traffic sign recognition represents a cornerstone technology for autonomous vehicles and intelligent transportation systems. This application leverages the German Traffic Sign Detection Benchmark dataset containing over 50,000 meticulously labeled images spanning diverse weather conditions, lighting scenarios, and sign deterioration states.

The system demonstrates remarkable versatility in identifying and classifying traffic signs across four primary categories:
- **Prohibitory signs**: Speed limits, no entry zones, restricted access
- **Danger warnings**: Intersection alerts, construction zones, hazard notifications  
- **Mandatory instructions**: Required directions, lane usage, vehicle-specific rules
- **Informational guidance**: Distance markers, route indicators, service locations

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/traffic_signs_dataset.png" title="German traffic signs dataset" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The comprehensive German Traffic Sign Detection Benchmark represents the gold standard for traffic sign recognition, providing the robust foundation necessary for autonomous vehicle navigation systems.
</div>

### PPE Detection System: Revolutionizing Construction Safety

Personal Protective Equipment detection addresses one of construction's most persistent challenges: ensuring consistent safety compliance across dynamic work environments. Traditional manual monitoring proves insufficient for large-scale operations, creating gaps that can lead to serious injuries or fatalities.

**Technical Specifications:**
- **Architecture**: YOLOv8 optimized for real-time inference
- **Training dataset**: 3,200 meticulously annotated instances
- **Data distribution**: 
  - Training: 2,991 instances (93.5%)
  - Validation: 119 instances (3.7%)  
  - Testing: 90 instances (2.8%)
- **Detection classes**: helmet, no helmet, vest, no-vest, person
- **Inference speed**: <100ms per frame on standard hardware

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
    **Left**: Precision-Recall curves reveal the model's ability to balance accuracy (precision) with completeness (recall) across different confidence thresholds. The area under each curve represents average precision, with higher values indicating superior performance. **Right**: The confusion matrix provides detailed insight into classification accuracy, with diagonal values representing correct predictions and off-diagonal elements revealing specific misclassification patterns that inform model improvements.
</div>

### Real-World Detection Performance

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ppe_detection_batch.png" title="PPE detection validation batch results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Validation results demonstrate robust performance across challenging real-world scenarios. The system successfully handles multiple workers simultaneously, varied poses, diverse lighting conditions, and cluttered backgrounds while maintaining high detection accuracy. Each prediction includes confidence scores and precise bounding boxes, enabling immediate safety assessments.
</div>

**Industry Impact Applications:**
- **Automated compliance monitoring**: Continuous safety oversight without human fatigue
- **Instant violation alerts**: Immediate notifications enable rapid safety interventions
- **Regulatory documentation**: Automated OSHA compliance reporting and audit trails
- **Predictive safety analytics**: Historical data analysis identifies high-risk areas and behaviors
- **Training enhancement**: Real violation examples improve safety education effectiveness

## Technical Innovation and Future Impact

This YOLOv8-based PPE detection system represents a paradigm shift from reactive to proactive safety management. By providing construction managers with real-time automated monitoring capabilities, the technology enables immediate response to safety violations while generating valuable data insights for long-term safety strategy development.

The system's deployment has demonstrated measurable impact in reducing workplace incidents through consistent monitoring standards that surpass human capability limitations. As construction sites increasingly adopt IoT sensors and connected safety systems, this computer vision foundation enables integration with broader safety ecosystems for comprehensive risk management.

**Key Technical Achievements:**
- Sub-100ms inference enabling real-time monitoring
- Robust performance across diverse environmental conditions  
- Scalable architecture supporting multiple concurrent camera feeds
- Edge deployment capability reducing latency and connectivity dependencies
- Continuous learning pipeline for model improvement using production data