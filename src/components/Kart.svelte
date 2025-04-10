<script lang="ts">
    // Address for the Google Maps link
    const address = "Vulkan Arena, Vulkan 26, 0178 Oslo, Norway";
    
    // Generate the Google Maps URL based on the address
    const googleMapsUrl = `https://www.google.com/maps?q=${encodeURIComponent(address)}`;
  </script>
  
  <style>
    .map-link {
      width: 100%;
      height: 150px; /* Set the height of the background image */
      background-image: url('/Users/norias/Documents/GitHub/svetle-test-typescript/img/kart.png'); /* Relative path to image in the public folder */
      background-size: cover; /* Ensure the image covers the entire container */
      background-position: center; /* Center the image */
      position: relative;
      cursor: pointer;
      text-align: center;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: transform 0.3s ease;
    }
  
    .map-link:hover {
      transform: scale(1.05); /* Slight zoom effect on hover */
    }
  
    .map-link:after {
      content: 'Click here to open Google Maps';
      color: white;
      background-color: rgba(0, 0, 0, 0.6);
      padding: 10px 20px;
      border-radius: 5px;
      font-size: 18px;
      font-weight: bold;
      position: absolute;
      bottom: 10px;
    }
  </style>
  
  <!-- Link with the background image -->
  <a class="map-link" href={googleMapsUrl} target="_blank">
    <!-- Optional text or content here -->
  </a>
  