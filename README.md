# **Spotify Listening Insights**  

## **Project Overview**
This report analyzes user behavior based on playback data from Spotify, focusing on metrics such as playback time, skipped tracks, platform usage, and track completion rates. The goal is to uncover listening trends, identify areas for improvement, and provide actionable recommendations.

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

---

### **Key Metrics and Insights**
#### 1. **Playback Time**  
- **Total Playback Time**: 5,280 hours of music played.
- **Average Playback Time Per Track**: 2 minutes.
- **Peak Listening Periods**:  
  - Most playback occurs during the **evening hours (6 PM - 12 AM)**, showing this is the most active period for listeners.
  - **Morning hours (6 AM - 12 PM)** also show considerable playback activity, likely tied to commute or work-related listening.

#### 2. **Tracks Played and Skipped**  
- **Total Tracks Played**: 16,000 tracks.
- **Skipped Tracks**: 18.54% of tracks were skipped.  
  - Skipping behavior varies significantly based on platform and time of day.  
- **Completion Rate**: 67.77% of tracks were completed.

#### 3. **Platform Insights**
- **Most Used Platform**: Android devices have the highest usage, likely due to the broad Android user base.  
- **Skip Rate by Platform**:  
  - **Windows** has the highest skip rate, meaning Windows users are more likely to skip tracks compared to their total playback.  
  - **Android** and **iOS** have lower skip rates, reflecting a more consistent listening experience.  
  - Windows users’ higher skip rate might result from multitasking or the convenience of skipping on a desktop platform.  

#### 4. **Top Artists and Tracks**  
- **Most Played Artists**: The Beatles, The Rolling Stones, and Imagine Dragons dominate the charts, indicating diverse preferences among users.  
- **Most Played Tracks**: "The Fellowship" and "Bright Lights" are the top favorites, reflecting the users' current musical trends.

#### 5. **Shuffle Mode**  
- **Shuffle Usage**: 32.15% of users listen in shuffle mode, showing a preference for randomized playback among a significant portion of users.  

#### 6. **Listening Trends Over Time**  
- **Trend Analysis**: Steady growth in listening activity is visible over the years, with notable spikes during holiday periods or major album releases.

---

### **Recommendations**
1. **Reduce Track Skipping on Windows**:  
-  Analyze the playlist and track recommendations for desktop users to improve engagement.  
- Consider implementing smarter track transitions or personalized playlists tailored to desktop activity.  

2. **Enhance Mobile Experience**:  
- Focus on optimizing the mobile user interface and introducing features such as dynamic playlists for Android and iOS users, as they form the majority of the audience.  

3. **Maximize Evening Listening**:  
- Create curated evening playlists or promote evening-focused campaigns to capitalize on the peak listening hours.  

4. **Promote Shuffle Mode Usage**:  
- Highlight shuffle mode in marketing campaigns or include shuffle-based challenges and curated lists to attract more randomized listeners.  

5. **Leverage Popular Artists and Tracks**:  
- Use insights from the top artists and tracks to drive marketing campaigns, such as promoting similar genres or creating themed playlists.

---

### **Steps Taken in Power BI**
1. **Data Import**:  
   The dataset was imported into Power BI and cleaned to ensure consistency. The fields included track name, artist name, ms_played, platform, shuffle mode, and reason for ending the track.  

2. **Transformations**:  
   - Created a new column to group playback times into time periods: Morning, Afternoon, Evening, and Night.  
   - Converted playback time from milliseconds to hours for better readability.  

3. **Visualizations**:  
   - **Card Visuals**: Displayed total playback time, average playback time, and total tracks played.  
   - **Bar Charts**: Showed most played tracks, skipped tracks, and platform usage.  
   - **Pie Charts**: Displayed skip rates and reasons for ending tracks.  
   - **Line Graph**: Highlighted listening trends over time.  

4. **Key Calculations**:  
     *Calculated Columns and Measures:*  
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

### **Conclusion**
The analysis provides a comprehensive understanding of user behavior on Spotify, revealing insights into listening trends, platform preferences, and track completion rates. Implementing the recommendations can enhance user engagement, reduce skipping behavior, and drive overall satisfaction.  

