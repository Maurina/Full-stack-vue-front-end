<template>
    <main>
        <form class="product-form" action="" method="POST">
            <div class="form-control">
                <label for="title">Title</label>
                <input type="text" name="title" id="title" value="">
            </div>
            <div class="form-control">
                <label for="imageUrl">Image URL</label>
                <input type="text" name="imageUrl" id="imageUrl" value="">
            </div>
            <div class="form-control">
                <label for="price">Date</label>
                <input type="number" name="date" id="date" step="0.01" value="">
            </div>
            <div class="form-control">
                <label for="description">Description</label>
                <textarea name="description" id="description" rows="5"></textarea>
            </div>
            <div class="update">
         <v-btn
                :disabled="valid"
                color="black white--text"
                rounded
                type="submit"
                @click="onSubmit(formData)"
            >
            Update
            </v-btn>
                 <v-btn
                :disabled="valid"
                color="red white--text"
                rounded
                type="submit"
                @click="onSubmit(formData)"
            >
            Delete
            </v-btn>
            </div>
        </form>
    </main>
</template>

<style scoped>
main{
    background-color: white;
    width: 25%;
    border-radius: 1rem;
    padding: 2%;
    margin: 0 auto;
}
.form-control{
    display: flex;
    flex-direction: column;
    padding-top: 3%;
}

input, textarea{
    border: 1px solid #999;
    border-radius: 1rem;
}

.update{
padding-top: 3%;
display: flex;
justify-content: space-evenly;
}
</style>