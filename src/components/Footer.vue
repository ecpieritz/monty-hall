<template>
  <div class="footer">
    <h3>Developed with 💙 by Emilyn C. Pieritz</h3>
    
    <div class="links">
    <a href="https://www.linkedin.com/in/ecpieritz/" target="_blank" rel="noopener noreferrer">
      <img id="linkedin" src="https://cdn.jsdelivr.net/npm/simple-icons@3.13.0/icons/linkedin.svg" alt="Linkedin">
    </a>

    <a href="https://www.instagram.com/ecpieritz/" target="_blank" rel="noopener noreferrer">
      <img id="instagram" src="https://cdn.jsdelivr.net/npm/simple-icons@3.13.0/icons/instagram.svg" alt="Instagram">
    </a>
    
    <a href="https://github.com/ecpieritz" target="_blank" rel="noopener noreferrer">
      <img id="instagram" src="https://cdn.jsdelivr.net/npm/simple-icons@3.13.0/icons/github.svg" alt="Instagram">
    </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style>
.footer{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  background-color: #fff6;
  width: 100vw;
  padding: 10px 20px;
  position: absolute;
  bottom: 0;
  color: #000;
}

.footer .links{
  margin: auto 0;
  display: flex;
  flex-direction: row;
  width: 100px;
  justify-content: space-between;
}

.links #linkedin, .links #instagram, .links #github{
  width: 25px;
}
</style>