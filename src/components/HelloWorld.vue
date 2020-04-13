<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="md-4">
        <v-item-group multiple>
          <v-container>
            <v-row>
              <v-col v-for="video in videos" :key="video.id" cols="12" md="4">
                <v-item>
                  <v-card class="mx-auto" max-width="344">
                    <v-img :src="video.thumbnail" height="200px"></v-img>
                    <v-card-title>
                      {{ video.title }}
                    </v-card-title>
                    <v-card-subtitle>
                      {{ video.tags }}
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
export default {
  name: 'HelloWorld',

  data: () => ({
    videos: [{
        'id': 1,
        'title': 'Django e VueJS #01 - arquivos estáticos via cdn',
        'tags': 'django,vuejs',
        'thumbnail': 'https://i.ytimg.com/vi/KOMER5MhBlY/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLDQC1fAIAzh3xNUiZY6lPsRK8yEDA'
      },
      {
        'id': 2,
        'title': 'Django e VueJS #02 - vue-cli e estáticos no Django',
        'tags': 'django,vuejs',
        'thumbnail': 'https://i.ytimg.com/vi/Ky6NddJTaMU/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLAlhslg4TkrHXLmXNMON8Qfrta5QQ'
      },
      {
        'id': 3,
        'title': 'Django e VueJS #03 - backend e frontend separados',
        'tags': 'django,vuejs',
        'thumbnail': 'https://i.ytimg.com/vi/FIyaGt6lNzU/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLB6-_rwMCVupyMTZD61i0lU_DDc0w'
      },
      {
        'id': 4,
        'title': 'Django e VueJS #04 - Django Rest Framework e VueJS',
        'tags': 'django,vuejs',
        'thumbnail': 'https://i.ytimg.com/vi/IkgG3piJ8KI/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLCKB8rpsQpI8BSXmgLmwUihpLgUqQ'
      },
      {
        'id': 5,
        'title': 'Backend e Frontend - Live com Alefe Souza',
        'tags': 'django,vuejs',
        'thumbnail': 'https://i.ytimg.com/vi/GAuyC5khFoc/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLCmtoO1GKcSQtHFVbplX3EMiJDecw'
      },
    ]
  }),
}
</script>