<template>
    <ApolloQuery :query="require('../graphql/AllCards.gql')"
    :variables="{ searchString }">
    <template v-slot="{ result: { loading, error, data } }">
        <!--Loading-->
        <div v-if="loading" class="loading apollo"> Loading...</div>

        <!--Error-->
        <div v-else-if="error" class="error apollo"> An error occured</div>

        <!--Result-->
        <div v-else-if="data" class="result apollo">
            <v-row>
                <v-col cols="4" v-for="(item, i) in data.Cards" :key="i">
                    <v-card class="mx-auto" max-width="350">
                        <v-card-text>
                            <div class="title"> {{ item.title }} </div>
                            <p>
                                {{ item.description }}
                            </p>
                            <p>{{ item.source }} </p>
                            <p> {{ item.keywords }} </p>
                        </v-card-text>
                        <v-card-action>
                            <v-btn text color="#000000">
                                Manage
                            </v-btn>
                        </v-card-action>
                    </v-card>
                </v-col>
            </v-row>
        </div>

        <!--no results-->
        <div v-else class="no-result apollo"> No result </div>
    </template>
  </ApolloQuery>
</template>

<script>
//import vue-truncate-filter from 'vue-truncate-filter'

export default {
  name: 'GraphqlDisplayCards',

  data: () => ({
    searchString: "Earth"
  }),
}
</script>

<style scoped>
.result {
  padding: 1rem;
}

.title {
  font-size: 1.25rem;
  font-weight: 600;
}
</style>
