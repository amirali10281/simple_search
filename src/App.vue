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
    <div style="display: flex; justify-content: center;">
      <div class="grid-container-overflow-y">
        <div v-for="  element, index in elements" :key="index" class="grid-item"
          :class="{ 'scroll-snap': index % 3 == 0 }">
          <item :item="element" />
        </div>
      </div>
    </div>

  </div>
</template>

<script>
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
  }
}
</script>

<style>

</style>