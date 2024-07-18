<template>
  <div class="main-container">
    <div class="resume-card">
      <h2>Resume</h2>
      <button @click="downloadResume">Download</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    downloadResume() {
      const link = document.createElement('a');
      link.href = '../assests/AmirZaman-Resume.pdf';
      link.download = 'Resume.pdf';
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    }
  }
}
</script>

<style scoped>
.main-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.resume-card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width:70%;
  padding: 20px;
  background-color: white;
  border-radius: 25px;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}

button {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #007BFF;
  color: white;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>
