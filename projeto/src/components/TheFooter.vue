<template>
  <div id="footer" class="bg-blue-solid">
    <div class="d-flex align-items-center">
      <div class="line-divider w-100"></div>
      <div>
        <img src="../assets/footer/laco.png" alt="" />
      </div>
      <div class="line-divider w-100"></div>
    </div>

    <div class="footer-container">
      <div class="d-flex justify-content-center p-5">
        <button class="mx-5">Dúvidas</button>
        <button class="mx-5">Regulamento</button>
      </div>

      <div class="d-flex justify-content-around">
        <img src="../assets/footer/redes-twitter.png" alt="" />
        <img src="../assets/footer/redes-facebook.png" alt="" />
        <img src="../assets/footer/redes-instagram.png" alt="" />
        <img src="../assets/footer/redes-yt.png" alt="" />
      </div>

      <p class="footer-text pt-5 pb-3">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iure neque nam
        beatae ratione sit laboriosam consectetur, eum natus minima pariatur
        soluta totam nisi amet suscipit dolor dolorem accusamus veniam odit,
        eligendi, culpa perspiciatis debitis ipsum fugiat? Beatae fugit fuga
        nesciunt velit officia numquam! Alias quod suscipit, nesciunt recusandae
        qui eveniet illo iusto omnis illum quis dolore
      </p>

      <div>
        <img src="../assets/footer/unilever.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TheFooter",
};
</script>

<style scoped>
#footer {
  padding: 38px 80px;
  color: white;
}

.line-divider {
  height: 1px;
  border: 1px solid white;
}

.footer-container {
  padding: 0 148px;
}

.footer-container button {
  font-family: "BrandonGrotesqueBlack", sans-serif;
  text-transform: uppercase;
  background-color: transparent;
  border: none;
  color: white;
}

.footer-text {
  font-size: 12px;
  line-height: 16px;
}

@media screen and (max-width: 992px) {
  #footer {
    padding: 38px 38px;
  }

  .footer-container {
    padding: 0 38px;
  }
}
</style>
