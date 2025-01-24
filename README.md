
---

# Spotify Listening Insights 
 
## **Project Overview**

This project dives deep into Spotify listening behavior. Using Power BI, I created a dashboard to visualize how users interact with tracks—what they love, when they listen most, and what they skip. Here’s everything you need to know about the dashboard, the insights it provides, and how I built it.  

---

## **Data Source**:
From Maven Analytics

---

## **Overview of the Dashboard**  

The dashboard is split into two pages:  
- **Page 1:** Gives a broad overview of listening habits, most played tracks, skip patterns, and platform usage.
![Image](https://github.com/user-attachments/assets/cd56b199-8931-4820-946f-eeff796e62a7)


- **Page 2:** Focuses on deeper analysis, such as when people are most active, skip rates across platforms, and most popular artists.  
![Image](https://github.com/user-attachments/assets/cca239f9-be23-4ece-bbc6-fc310790d666)

Here are the main metrics and visuals I’ve included: 

### **Page 1: Listening Overview**  
1. **Total Playback Time (5,280 hours):**  
   Shows the total time users spent listening to tracks, converted from milliseconds into hours.  

2. **Track Time (2 minutes):**  
   The average time spent on each track, giving insight into track engagement.  

3. **Tracks Played (16,000):**  
   Total number of tracks streamed over the dataset period.  

4. **Total Days (2,715):**  
   This represents the span of the data (from the first to the last timestamp).  

5. **Most Played Tracks:**  
   A bar chart that highlights tracks with the highest playback time. For example, “The Fellowship” was streamed the most.  

6. **Skipped Tracks:**  
   A pie chart showing how many tracks users skipped versus completed.  

7. **Reason for Ending Tracks:**  
   Pie chart breaking down why a track ended—was it skipped, completed, or interrupted?  

8. **Trends Over Time:**  
   A line chart that visualizes listening patterns across different years, showing how user engagement has changed over time.  

9. **Most Used Platform:**  
   A bar chart showing which platforms (Android, iOS, Web Player, etc.) were most popular for streaming.  

10. **Shuffle Mode:**  
    A pie chart showing how often users utilized shuffle mode while listening to tracks.  

---

### **Page 2: In-Depth Analysis**  
1. **Play Time by Period (Morning, Afternoon, Evening, Night):**  
   A bar chart that analyzes when users listen to music the most, grouped into time periods. For example, mornings and evenings show higher engagement, reflecting commute or downtime habits.  

2. **Skip Rate by Platform:**  
   A bar chart that shows which platforms had the highest skip rates, giving insights into platform usability or user behavior.  

3. **Completion Rate:**  
   A pie chart showing how often tracks were fully played versus skipped.  

4. **Most Played Artists:**  
   A bar chart listing the top artists by playback time, with bands like “The Beatles” and “The killers” ranking high.  

5. **Skip Rate by Time Period:**  
   A line chart showing how skip rates vary throughout the day. For instance, users tend to skip tracks more in the evening compared to the afternoon.  

---

## **Key Insights from the Dashboard**  

- **Listening Habits:**  
   Users listen the most during mornings and evenings, likely corresponding to commutes or relaxation time.  

- **Engagement Patterns:**  
   The average playback time per track is 2 minutes, suggesting many users either skip early or prefer shorter tracks.  

- **Platform Preferences:**  
   Android is the most used platform, followed by Web Player. Interestingly, Android users also had the highest skip rates.  

- **Top Tracks & Artists:**  
   Certain tracks like *“The Fellowship”* and artists like *The Beatles* dominate playback time, showing high user loyalty to these artists.  

- **Shuffle Usage:**  
   Shuffle mode was used only 32% of the time, indicating that most users prefer to control their listening order.  

---
## **Recommendations:**
**Optimize Track Length:**
Consider reducing the average track length or providing users with shorter versions of songs to decrease skip rates.

**Focus Marketing Efforts During Peak Hours:**
Schedule promotional campaigns, new releases, and ads for morning (8 AM - 11 AM) and evening (6 PM - 9 PM) to maximize engagement.

**Enhance Android Experience:**
Invest in improving playback features and user experience on Android, as it’s the most used platform.

**Personalized Playlists:**
Use insights from skipped tracks to curate playlists tailored to user preferences, reducing the likelihood of skips.

---
**Engage During Evenings:**
Encourage evening listening with calming or thematic playlists to align with user behavior.

**Artist Promotion:**
Highlight popular artists (e.g., The Beatles) to capitalize on existing listening trends and introduce similar genres or artists.

## **Steps to Build the Dashboard in Power BI**  

Here’s how I built the dashboard from the ground up:  

### **Data Preparation**  
1. **Dataset Overview:**  
   The dataset includes columns like `spotify_track_uri`, `artist_name`, `platform`, `ms_played`, and more.  

2. **Calculated Columns and Measures:**  
   - Converted `ms_played` into hours for readability:  
     ```DAX
     Playback Hours = SUM('Data'[ms_played]) / 3600000
     ```  
   - Average playback time:  
     ```DAX
     Avg Track Time = AVERAGE('Data'[ms_played]) / 60000
     ```  
   - Total days in the dataset:  
     ```DAX
     Total Days = DATEDIFF(MIN('Data'[ts]), MAX('Data'[ts]), DAY)
     ```  

---

### **Building Visuals in Power BI**  
1. Drag fields into visualizations, such as bar charts, pie charts, and line graphs.  
2. Format visuals using consistent green color themes to reflect Spotify branding.  
3. Use slicers for filters like Date, Artist, and Platform to allow dynamic filtering.  

---

## **How to Use the Dashboard**  

1. **Identify Listening Trends:**  
   Use the “Trends Over Time” chart to analyze how user engagement evolved.  

2. **Analyze Playback Patterns:**  
   Focus on the “Play Time by Period” chart to determine when users are most active.  

3. **Understand User Behavior:**  
   Use the “Skipped Tracks” and “Reason for Ending Track” visuals to uncover why tracks are skipped.  

4. **Optimize Platform Performance:**  
   The “Skip Rate by Platform” chart helps identify which platforms might need improvement.  

---

## **Conclusion**  

This dashboard highlights user engagement with Spotify, offering insights into track performance, listening patterns, and platform usage. The findings can guide decisions like optimizing track lengths, improving platform interfaces, or targeting marketing efforts during peak listening times.  

---


