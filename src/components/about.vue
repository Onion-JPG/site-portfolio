<script lang="ts">
import colorText from "./colorText.vue";

export default {
  name: "about",
  data() {
    return {
      aboutLine1: true,
      aboutLine2: false,
      aboutLine3: false,
      aboutLine4: false,
      aboutLine5: false,
      aboutLine6: false,
      aboutLine7: false,
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

<style>
  .pl-6 {
    padding-left: 1.5rem;
  }

</style>

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
      <!-- block 1 -->
      <div class="text-[#FFB0AE] italic pl-3 flex flex-wrap">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine1"
          @printDone="aboutLine2 = true"
          printableText="// Hi my name is Caden Citro A.K.A Onion_jpg"
        ></colorText>
      </div>

      <!-- block 2 -->
      <div class="text-[#FFB0AE] italic pl-3 flex flex-wrap">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine2"
          @printDone="aboutLine3 = true"
          printableText="// I am a student studying Computer Science and Games at Miami University"
        ></colorText>
      </div>

      <!-- block 3 -->
      <div class="pl-3">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine3"
          @printDone="aboutLine4 = true"
          printableText="Links = {"
        ></colorText>
      </div>

      <!-- block 4 -->
      <div class="pl-6 flex flex-row">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine4"
          @printDone="aboutLine5 = true"
          printableText="Github: "
        ></colorText>
        <a
          v-if="aboutLine5"
          class="text-400"
          href="https://github.com/Onion-JPG/portfolio"
          target="_blank"
          >github.com/Onion-JPG/portfolio</a
        >
      </div>

      <!-- block 5 -->
      <div class="pl-6 flex flex-row">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine5"
          @printDone="aboutLine6 = true"
          printableText="LinkedIn: "
        ></colorText>
        <a
          v-if="aboutLine6"
          class="text-400 underline"
          href="https://www.linkedin.com/in/caden-citro/"
          target="_blank"
          >linkedin.com/in/caden-citro/</a
        >
      </div>

      <!-- block 5 -->
      <div class="pl-6 flex flex-row">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine6"
          @printDone="aboutLine7 = true"
          printableText="Example of Work: "
        ></colorText>
        <a
          v-if="aboutLine7"
          class="text-400 underline"
          href="https://redhawks.gg/"
          target="_blank"
          >redhawks.gg</a
        >
      </div>

      <!-- block 6 -->
      <div class="pl-3">
        <colorText
          :printSpeed="20"
          :printStatus="aboutLine7"
          printableText="}"
        ></colorText>
      </div>

    </div>
  </div>
</template>
