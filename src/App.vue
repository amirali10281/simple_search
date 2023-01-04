<template>
  <div>
    <div style="display: flex; justify-content: center; position: static; height: 90px;">
      <NavBar style="width: 70%;" />
    </div>
    <div class="home-image">
      <ImageHome />
    </div>
    <div style="display: flex; justify-content: center;">
      <SearchField style="width:65%;" />
    </div>
    <div style="display: flex; justify-content: center; ">
      <div style="height: 100%; position: relative;width: 100%;">
        <div class="grid-container-overflow-y" id="items">
          <div v-for="  element, index in elements" :key="index" class="grid-item"
            :class="{ 'scroll-snap': index % howManyItems == 0 }">
            <item :item="element" class="animated" />
          </div>
        </div>
        <div class="slider">
          <div
            style="position: absolute; top:30px ; left: 0; right: 0; bottom: 70px;background-image: linear-gradient(to bottom right, rgb(255, 26, 232), rgba(85, 0, 164,0));; border-radius: 1rem; ">
          </div>
        </div>
        <button class="navbutton" style="right: 10px;" @click="scrollMe(1)">
          <i class="fa fa-arrow-right" style="font-size:24px"></i>
        </button>
        <button class="navbutton" style="left:10px" @click="scrollMe(-1)">
          <i class="fa fa-arrow-left" style="font-size:24px"></i>
        </button>
      </div>

    </div>
  </div>
</template>

<script>
import { computed } from '@vue/runtime-core';
import ImageHome from './components/ImageHome.vue';
import Item from './components/Item.vue';
import NavBar from './components/NavBar.vue';
import SearchField from './components/SearchField.vue';

export default {
  components: { SearchField, NavBar, Item, ImageHome },


  data() {
    return {
      elements: [
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
        {
          title: "title",
          picInfo: "item-image-text",
          writer: "description",
          description: "description",
          image: "sample",
          reviews: 4.7,
          otherInfo: 'Intermediate.Specialiation.3.6months',
          star: 5
        },
      ],
    }
  },
  methods: {
    scrollMe(direction) {
      document.getElementById('items').scrollBy(direction, 0)
      console.log("width:", window.innerWidth)
    },
  },
  computed: {
    howManyItems() {
      return parseInt(window.innerWidth / 300);
    }
  }
}
</script>

<style>

</style>