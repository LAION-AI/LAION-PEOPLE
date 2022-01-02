# LAION-PEOPLE
This project provides a data set with bounding boxes, body poses, 3D face meshes &amp; captions of people from our LAION-2.2B. Additionally it provides clusters based on the poses and face meshes and pose-related captions based on these cluster assignments.
---

**Step 1 - Data extraction:**


**Step 2 - CLIP filtering of image level captions w.r.t. the person bounding boxes:**
-> SUBSET A: Dataset of person bounding boxes & captions from the source image, that still seem to fit well together (similarity >0.3).


**Step 3 - Clustering:**
-> SUBSET B: Dataset of ...

  1.) images showing 2 or more person bounding boxes in front of a random background image & 
  2.) pose & face mesh related similarity captions like e.g. 

      "The image shows two people, both of them have similar body poses. /
      "There are two people in the picture with different body poses." 
      "Here you see three people. The body parts of 2 of them are in similar positions."
      "This image shows two people with similar/different face meshes/ head positions/ ... ."


**Step 4 - Pose- & face- related labeling of the clusters with each several cannidate captions:**


**Step 5 - Assignment of pose- and face-related captions to each cluster member using CLIP:**
-> SUBSET C: Dataset of person bounding box image - text pairs, where the text describes the body pose & facial expression without relating to other image features like clothes, age, gender, ...  --> One potential appication of this would be to add this data to general purpose image generation models to teach them to consider fine details of poses and head-related details, when generating images of person guided by natural language. This could be very useful for art, language guided selfie manipulation & content creation for video games and advertisement.


**Experimental idea - Generate detailed captions for each bounding box image by using SOTA captioning models (like e.g. MAGMA or SimVLM ) & filtering them with CLIP:**
