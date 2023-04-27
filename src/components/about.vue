<script lang="ts">
import colorText from "./colorText.vue";

export default {
  name: "about",
  data() {
    return {
      aboutLine1: true,
      aboutLine2: false,
      displayAbout: true,
    };
  },
  components: {
    colorText,
  },
  props: {
    displayProject: Boolean,
  },
};
</script>

<template>
  <div
    class="container rounded-lg w-[700px] m-2 relative mb-24"
    style="background-color: #2a2a2a"
  >
    <div class="flex flex-row">
      <div
        class="container flex justify-start text-white p-2 gap-2"
        style="width: 75%"
      >
        <button
          class="rounded-full w-5 h-5 bg-[#00CA4E] hover:bg-[#33D571]"
        ></button>
        <button
          class="rounded-full w-5 h-5 bg-[#FFBD44] hover:bg-[#FFCA69]"
        ></button>
        <button
          class="rounded-full w-5 h-5 bg-[#FF605C] hover:bg-[#FF807D]"
        ></button>
      </div>
      <div class="container flex text-white p-2 pl-4 italic">
        <h2>About Me</h2>
      </div>
    </div>

    <div
      class="container bg-slate-400 min-h-[260px] rounded-bl-lg rounded-br-lg text-white p-2 font-mono"
      style="background-color: #191919"
    >
      <div class="text-[#FFB0AE] italic pl-3 flex flex-wrap">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine1"
          @printDone="aboutLine2 = true"
          printableText="// Hi my name is Caden Citro A.K.A Onion_jpg"
        ></colorText>
      </div>
      <div class="text-[#FFB0AE] italic pl-3 flex flex-wrap">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine2"
          printableText="// I am a student studying Computer Science and Games at Miami University"
        ></colorText>
      </div>
    </div>
  </div>
</template>
