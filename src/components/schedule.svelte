<script lang="ts">
    // Define a type for the schedule items
    type ScheduleItem = {
      time: string;
      event: string;
      description: string;
    };
  
    // Define the schedule array for one day
    const schedule: ScheduleItem[] = [
      { time: "08:30", event: "Registration and breakfast", description: "" },
      { time: "08:55", event: "Intro", description: "Focus on completing project tasks." },
      { time: "09:00", event: "Keynote - Exploring the World of Ethical Hacking: From Web Vulnerabilities to Election Security - Hallvard Nygård", description: "Take a break and enjoy a meal." },
      { time: "09:45 ", event: "SSH authentication using user and machine identities - Morten Linderud", description: "In this talk, Hallvard will dive into the process of identifying and reporting security flaws in publicly available web solutions. Through responsible disclosure, he helps organizations fix vulnerabilities, learning and sharing insights along the way — often with a bit of fun on Twitter or even news articles." },
      { time: "10:30 ", event: "Break", description: "Review and provide feedback on code." },
      { time: "10:55", event: "Chrome Browser Exploitation: from zero to heap sandbox escape - Matteo Malvica", description: "Finish up remaining tasks and plan for tomorrow." },
      { time: "11:40", event: "Post-compromise: Uncovering Clouds and Assessing at Lightning Speed - Karim El-Melhaoui", description: "Start your day with a light workout." },
      { time: "12:00", event: "Lunch", description: "Focus on completing project tasks." },
      { time: "13:00", event: "End-to-end Supply Chain Integrity - Stian Kristoffersen", description: "Take a break and enjoy a meal." },
      { time: "13:45", event: "Http Header Injections: a Splitting Headache - Sofia Lindqvist", description: "Collaborate with the team on current projects." },
      { time: "14:30", event: "Break", description: "Review and provide feedback on code." },
      { time: "14:55", event: "Tales of a Malspam Campaign from a Threat Actor's Perspective - Antonis Terefos", description: "Finish up remaining tasks and plan for tomorrow." },
      { time: "15:15", event: "Taking a Look at the Cyber Security of Modern Trains - Tom Chothia", description: "Start your day with a light workout." },
      { time: "16:00", event: "The Law of Jante (janteloven) in Cybersecurity - Breaking the myth of America's superiority over Norway - Kim Engebretsen", description: "Focus on completing project tasks." },
      { time: "16:20", event: "Closing note", description: "Take a break and enjoy a meal." },
      { time: "16:35", event: "Bar open at Pokalen", description: "Collaborate with the team on current projects." },
      { time: "17:45", event: " Dinner in Arena (for those who signed up)", description: "Review and provide feedback on code." },
      { time: "21:30", event: "Bar closes", description: "Finish up remaining tasks and plan for tomorrow." },
      { time: "22:00", event: "Event closed", description: "Finish up remaining tasks and plan for tomorrow." },
    ];
  </script>
  
  <style>
    .schedule-container {
      max-width: 600px;
      margin: 20px auto;
      padding: 20px;
      font-family: Arial, sans-serif;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
  
    h2 {
      text-align: center;
      font-size: 24px;
      margin-bottom: 20px;
      color: #333;
    }
  
    .schedule-list {
      list-style-type: none;
      padding: 0;
    }
  
    .schedule-item {
      display: flex;
      justify-content: space-between;
      padding: 15px;
      margin-bottom: 10px;
      background-color: #f9f9f9;
      border-radius: 5px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }
  

    .schedule-item p {
      font-size: 14px;
      color: #555;
    }
  
    .schedule-item:hover {
      background-color: #f1f1f1;
    }
  </style>
  
  <div class="schedule-container">
    <h2>Today's Schedule</h2>
  
    <!-- Display the list of schedule items -->
    <ul class="schedule-list">
      {#each schedule as { time, event, description }}
        <li class="schedule-item">
          <div>
            <strong>{time}:</strong>
            <h3>{event}</h3>
            <p>{description}</p>
          </div>
        </li>
      {/each}
    </ul>
  </div>
  