<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="md-4">
        <v-item-group multiple>
          <v-container>
            <v-row>
              <v-col v-for="video in filteredItems" :key="video.id" cols="12" md="3">
                <v-item>
                  <v-card class="mx-auto" max-width="260" min-height="320">
                    <v-img :src="video.thumbnail" width="260px"></v-img>
                    <v-card-title>
                      <div style="font-size: 15px">
                        <a :href="video.url" target="_blank" style="word-break: break-word !important;">{{ video.title }}</a>
                      </div>
                    </v-card-title>
                    <v-card-subtitle>
                      <a v-for="tag in video.tags" :key="tag" @click.prevent="selectedTag = tag">#{{ tag }} </a>
                    </v-card-subtitle>
                  </v-card>
                </v-item>
              </v-col>
            </v-row>
          </v-container>
        </v-item-group>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import data from '../data.json';

export default {
  name: 'Videos',
  props: ['search'],
  data() {
    return { ...data, selectedTag: '' };
  },
  computed: {
    filteredItems() {
      return this.videos.filter((item) => {
        return item.title.toLowerCase().indexOf(this.search.toLowerCase()) >= 0 || item.tags.includes(this.search.toLowerCase());
      }).filter((item) => {
        if (!this.selectedTag) { return true; }
        return item.tags.includes(this.selectedTag);
      });
    }
  }
}
</script>