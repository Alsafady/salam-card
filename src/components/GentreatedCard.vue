<template>
  Horizontal Card: Recommended for snapchat, whatsapp status, instagram stories
  <div class="card-area-h" id="card-area-h">
    <img
      src="/public/assets/card_h.png"
      alt=""
      width="357"
      height="625"
      class="d-inline-block pt-n5"
    />
    <div class="empNameH">
      {{ empName }}
    </div>
    <br />
    <div class="empNameEnH">
      {{ empNameEn }}
    </div>
  </div>

  <br />

  <div class="mt-4">
    <button
      type="button"
      class="btn btn-secondary btn-lg"
      @click="generateCardH()"
    >
      تــحميــل
    </button>
  </div>

  <br />
  <hr />
  <br />

  Vertical Card: Recommended for linkedin, Twitter, facebook

  <div class="card-area-v" id="card-area-v">
    <img
      src="/assets/card_v.png"
      alt=""
      width="600"
      height="315"
      class="d-inline-block pt-n5"
    />
    <div class="empNameV">
      {{ empName }}
    </div>
    <br />
    <div class="empNameEnV">
      {{ empNameEn }}
    </div>
  </div>

  <div class="mt-4">
    <button
      type="button"
      class="btn btn-secondary btn-lg"
      @click="generateCardV()"
    >
      تــحميــل
    </button>
  </div>
</template>
<script>
import html2canvas from 'html2canvas';

export default {
  name: 'GentreatedCard',
  props: {
    empName: String,
    empNameEn: String,
  },
  methods: {
    async generateCardH() {
      const canvas = await html2canvas(document.getElementById('card-area-h'));
      canvas.style.display = 'none';
      document.body.appendChild(canvas);
      const image = canvas
        .toDataURL('image/png')
        .replace('image/png', 'image/octet-stream');
      const a = document.createElement('a');

      a.setAttribute('download', `My-Salam-Hcard.png`);
      a.setAttribute('href', image);
      a.click();
    },

    async generateCardV() {
      const canvas = await html2canvas(document.getElementById('card-area-v'));
      canvas.style.display = 'none';
      document.body.appendChild(canvas);
      const image = canvas
        .toDataURL('image/png')
        .replace('image/png', 'image/octet-stream');
      const a = document.createElement('a');

      a.setAttribute('download', `My-Salam-Vcard.png`);
      a.setAttribute('href', image);
      a.click();
    },
  },
};
</script>
<style>
.card-area-h {
  position: relative;
  text-align: center;
  width: 357px;
  height: 625px;
  margin-left: auto;
  margin-right: auto;
}

.card-area-v {
  position: relative;
  text-align: center;
  width: 600px;
  height: 315px;
}

.empNameH {
  font-family: 'Tajawal', sans-serif !important;
  font-size: 20px;

  position: absolute;
  top: 57%;
  /*left: 35%;*/
  width: 100%;

  color: #002035 !important;
  /* transform: translate(-50%, -50%); */
}
.empNameV {
  font-family: 'Tajawal', sans-serif !important;
  font-size: 20px;

  position: absolute;
  top: 45%;
  right: 4%;
  width: 100%;

  color: #002035 !important;
  /* transform: translate(-50%, -50%); */
}

.empNameEnH {
  font-family: 'Tajawal', sans-serif !important;
  font-size: 20px;

  position: absolute;
  top: 84%;
  /*right: 4%;*/
  width: 100%;

  color: #002035 !important;
  /* transform: translate(-50%, -50%); */
}
.empNameEnV {
  font-family: 'Tajawal', sans-serif !important;
  font-size: 20px;

  position: absolute;
  top: 77%;
  right: 4%;
  width: 100%;

  color: #002035 !important;
  /* transform: translate(-50%, -50%); */
}
</style>
