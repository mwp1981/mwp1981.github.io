# Zingto Image Scoring Software - Frame Capture Module Operation Guide
This article will demonstrate the detailed functions and operation process of the "Frame Capture" module in the Zingto Image Scoring Software step by step. The tutorial will use a 4K video (file name: mixkit-friends-with-colored-smoke-bombs-4556-4k.mp4) provided by the free video website Mixkit as the practical video source to help you quickly master the core usage of the module.

## I. Description of Video Source and Objectives

### 1.1 Video Source Description

Video Content: On a sunny afternoon, young people play with colored smoke bombs on an open plain, with trees in the background on the horizon.

<p style="text-align: center; margin: 1.5rem 0;">
  <img src="/assets/images/zingto_frame_capture_module_Screenshot_a.png" alt="Description of Video Source" width="700" style="height: auto; border: 1px solid #eee; border-radius: 6px;">
</p>
<p style="color: #6a737d; font-size: 0.9rem; text-align: center; margin-top: -1rem; margin-bottom: 1.5rem;">Figure 1: Description of Video Source</p>

### 1.2 Core Operation Objectives

This practical operation needs to complete frame capture and optimal screening for 3 types of scenes. The specific objectives are as follows:

- Capture the image of the girl in the dress jumping to the highest point, and select the frame with the highest score;

- Capture the image of the girl in jeans jumping to the highest point, and select the frame with the highest score;

- Capture the image of both girls jumping at the same time, and select the frame with the highest score.

## II. Detailed Operation Steps

The following is the complete operation process. Please perform each step of configuration and operation in sequence:

### Step 1: Configure Frame Capture Parameters and Execute Capture

First, switch to the "Frame Capture" module tab of the software, and complete parameter configuration and video frame extraction according to the following steps:

1. Open the parameter configuration window: Click the [Select Video Source] button on the interface to pop up the "Frame Capture Parameters Configuration" window;

2. Select the video parsing tool: The default option in the Video Tool drop-down box is OpenCV. If the video to be processed has a high compression rate, resulting in slow frame extraction, you can switch to FFmpeg mode to improve parsing efficiency;

3. Enable high-frequency frame capture mode: This option is not checked by default, and the default minimum capture interval is 3 seconds. Since we need to accurately capture the moment the girls jump in the demo, we need to check "Enable High-Frequency Frame Capture Mode" and set the "Capture Interval" to 0.1 seconds;

4. Set the capture time range: Capture Start Time and Capture End Time are used to define the total duration of frame capture. After enabling the high-frequency frame capture mode, the system defaults to limit the total capture duration to no more than 60 seconds;

5. Configure image size: The 4K demo video for this practical operation has a default frame width of 3840px and height of 2160px. If you need to reduce storage usage, you can set the size to 1/2 or 1/3 of the original size;

6. Set the image prefix name: The default prefix is "screenshot". You can modify it to a custom name (example: mixkit_friends_with_colored_smoke_bombs) according to your needs to facilitate subsequent file identification;

7. Start frame capture: After completing all the configuration parameters that need to be modified, click the [Start Capture] button. The software will automatically parse the video and save the frame images to the specified local directory.

<p style="text-align: center; margin: 1.5rem 0;">
  <img src="/assets/images/zingto_frame_capture_module_Screenshot_b.png" alt="Configure Frame Capture Parameters" width="700" style="height: auto; border: 1px solid #eee; border-radius: 6px;">
</p>
<p style="color: #6a737d; font-size: 0.9rem; text-align: center; margin-top: -1rem; margin-bottom: 1.5rem;">Figure 2: Configure Frame Capture Parameters</p>

### Step 2: Image Scoring and Target Frame Screening

After the frame capture is completed, switch to the "Image Scoring" module tab, and complete image scoring and target scene screening according to the following steps:

1. Load the captured frame images: Click the [Open Image Folder] button on the interface and select the save directory of the frame images in Step 1;

2. Automatic scoring and sorting: The software will automatically score all images in the directory. The scoring results will be displayed in the "Image List" and sorted in descending order of score by default;

<p style="text-align: center; margin: 1.5rem 0;">
  <img src="/assets/images/zingto_frame_capture_module_Screenshot_c.png" alt="Image Scoring List" width="700" style="height: auto; border: 1px solid #eee; border-radius: 6px;">
</p>
<p style="color: #6a737d; font-size: 0.9rem; text-align: center; margin-top: -1rem; margin-bottom: 1.5rem;">Figure 3: Image Scoring List</p>

3. Screen target scene frames: Browse the sorted Image List to locate and screen out the images that meet the 3 core objectives mentioned earlier. The 3 example images (including the optimal frames of the target scenes) obtained after my actual operation are as follows for reference (the actual results are subject to the personal operating environment):

<p style="text-align: center; margin: 1.5rem 0;">
  <img src="/assets/images/zingto_frame_capture_module_screenshot_1.jpg" alt="the girl in the dress jumping to the highest point" width="700" style="height: auto; border: 1px solid #eee; border-radius: 6px;">
</p>
<p style="color: #6a737d; font-size: 0.9rem; text-align: center; margin-top: -1rem; margin-bottom: 1.5rem;">Figure 4: the girl in the dress jumping to the highest point</p>

<p style="text-align: center; margin: 1.5rem 0;">
  <img src="/assets/images/zingto_frame_capture_module_screenshot_2.jpg" alt="the girl in jeans jumping to the highest point" width="700" style="height: auto; border: 1px solid #eee; border-radius: 6px;">
</p>
<p style="color: #6a737d; font-size: 0.9rem; text-align: center; margin-top: -1rem; margin-bottom: 1.5rem;">Figure 5: the girl in jeans jumping to the highest point</p>

<p style="text-align: center; margin: 1.5rem 0;">
  <img src="/assets/images/zingto_frame_capture_module_screenshot_3.jpg" alt="both girls jumping at the same time" width="700" style="height: auto; border: 1px solid #eee; border-radius: 6px;">
</p>
<p style="color: #6a737d; font-size: 0.9rem; text-align: center; margin-top: -1rem; margin-bottom: 1.5rem;">Figure 6: both girls jumping at the same time</p>

## III. Operation Summary

The above is the complete practical operation process of frame capture and image scoring in Zingto software. By reasonably configuring frame capture parameters (especially high-frequency capture mode and capture interval), you can accurately capture key moments in the video, and quickly screen out the optimal frame images combined with the automatic scoring function.

If you have further questions about the functions of this module or need assistance during the operation, please feel free to leave a message for communication, and I will reply to you in a timely manner!

## Keywords

Zingto Image Scoring Software, Frame Capture Module, video frame extraction, image scoring, 4K video frame capture

