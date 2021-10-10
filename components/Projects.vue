<template>
  <v-row dense>
    <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
      <v-hover v-slot="{ hover }">
        <v-card>
          <v-img
            :src="card.src"
            class="white--text align-end"
            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="400px"
          >
            <v-expand-transition>
              <div
                v-if="hover"
                class="
                  d-flex
                  transition-fast-in-fast-out
                  v-card--reveal
                  text-body-1 text-justify
                  white--text
                "
                style="height: 100%"
              >
                {{ card.description }}
              </div>
            </v-expand-transition>
            <v-card-title v-text="card.title"></v-card-title>
          </v-img>

          <v-card-actions>
            <v-list-item>
              <v-row align="left" justify="space-between">
                <div>
                  <v-btn
                    v-for="(icon, index) in icons"
                    :key="index"
                    :class="{ 'show-btns': hover }"
                    :color="transparent"
                    icon
                  >
                    <v-icon
                      :class="{ 'show-btns': hover }"
                      :color="transparent"
                    >
                      {{ icon }}
                    </v-icon>
                  </v-btn>
                </div>

                <v-btn icon fab dark small color="pink">
                  <v-icon>mdi-heart</v-icon>
                </v-btn>
              </v-row>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </v-hover>
    </v-col>
  </v-row>
</template>

<script>
import text from '@/assets/txt/lorem.txt'
import anelog from '@/assets/img/anelog.png'
import spejlvendt from '@/assets/img/spejlvendt.png'
export default {
  data: () => ({
    cards: [
      {
        title: 'Anelog',
        src: anelog,
        flex: 6,
        description: text,
      },
      {
        title: 'Spejlvendt',
        src: spejlvendt,
        flex: 6,
        description: text,
      },
      
    ],
    icons: ['mdi-rewind', 'mdi-play', 'mdi-fast-forward'],
  }),
}
</script>

<style></style>
