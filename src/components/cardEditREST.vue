<template>
 
    <main>
        <form class="product-form" action="/admin/<% if (editing) { %>edit-product<% } else { %>add-product<% } %>" method="POST">
            <div class="form-control">
                <label for="title">Title</label>
                <input type="text" name="title" id="title" value="<% if (editing) { %><%= product.title %><% } %>">
            </div>
            <div class="form-control">
                <label for="imageUrl">Image URL</label>
                <input type="text" name="imageUrl" id="imageUrl" value="<% if (editing) { %><%= product.imageUrl %><% } %>">
            </div>
            <div class="form-control">
                <label for="price">Date</label>
                <input type="number" name="date" id="date" step="0.01" value="<% if (editing) { %><%= product.date %><% } %>">
            </div>
            <div class="form-control">
                <label for="description">Description</label>
                <textarea name="description" id="description" rows="5"><% if (editing) { %><%= product.description %><% } %></textarea>
            </div>
          
                <input type="hidden" v-model="id" name="productId">
            

            <button class="btn" type="submit"><% if (editing) { %>Update Card<% } else { %>Add Card<% } %></button>
        </form>
    </main>
</template>

<script>
export default {
  data: function() {
    return {
      title: '',
      description: '',
      keywords: [],
      source: '',
      image: '',
      productId:''
    }
  },
  methods: {
    onDone() {
      return console.log('Done')
    }
  }
}
</script>