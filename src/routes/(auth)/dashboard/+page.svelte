<script>
    let pythonCode = '';
    let pythonFile = null;
  
    // Handle file upload
    const handleFileUpload = (event) => {
      const file = event.target.files[0];
      pythonFile = file;
      console.log('Uploaded file:', file);
      // Handle the file logic here (e.g., reading the file content)
    };

    import PortfolioBar from "../../../lib/components/PortfolioBar.svelte";
  </script>
  
  <div class="dashboard-layout">
      <PortfolioBar />
  </div>
  
  <style>
    .dashboard-layout {
      margin: 0;
      display: block;
    }
  </style>
  