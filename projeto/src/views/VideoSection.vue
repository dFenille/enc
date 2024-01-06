<template>
  <div id="video" class="bg-blue-solid">
    <div class="title-container">
      <h2>
        Dos dribles e enterradas memoráveis ao zerar do cronômetro, <br />
        cada hora H da NBA fica ainda mais saborasa com Hellmann's.
      </h2>
      <h1>Assista ao filme abaixo:</h1>
    </div>

    <iframe
      title="Hora H da NBA com Hellmann's"
      src="https://www.youtube.com/embed/KAIR1_wOJvg"
      frameborder="0"
      allowfullscreen
      class="iframe"
    ></iframe>
  </div>
</template>

<script>
export default {
  name: "VideoSection",
};
</script>

<style scoped>
#video {
  font-family: "BrandonGrotesqueBlack", sans-serif;
  text-transform: uppercase;
  padding: 38px 148px;
  color: white;
}

.title-container {
  padding: 48px;
}

.iframe {
  width: 100%;
  height: 630px;
  max-width: 1020px;
  padding-bottom: 12px;
}

@media screen and (max-width: 1128px) {
  .title-container {
    padding: 24px;
  }

  .iframe {
    width: 100%;
    height: 540px;
  }
}

@media screen and (max-width: 768px) {
  #video {
    padding: 38px 24px;
  }

  .iframe {
    width: 100%;
    height: 420px;
  }
}
</style>
