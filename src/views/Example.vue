<template>
  <div class="container">
        <table class="table table-striped">
          <thead>
            <tr>
              <th>No</th>
              <th>Name</th>
              <th>Address</th>
              <th>Phones</th>
            </tr>
          </thead>
          <tbody>
              <tr>
                  <td>1</td>
                  <td>Mark Watney</td>
                  <td>California CA</td>
                  <td>08557766881</td>
              </tr>
              <tr>
                  <td>2</td>
                  <td>Mark Watney</td>
                  <td>California CA</td>
                  <td>08557766881</td>
              </tr>
              <tr>
                  <td>3</td>
                  <td>Mark Watney</td>
                  <td>California CA</td>
                  <td>08557766881</td>
              </tr>
              <tr>
                  <td>4</td>
                  <td>Mark Watney</td>
                  <td>California CA</td>
                  <td>08557766881</td>
              </tr>
          </tbody>
        </table>

        <!-- Data seko api -->
        <h1>Data dari API</h1>
        {{ posts }}
      </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'example-pages',
  data: function() {
    return {
      posts: []
    }
  },
  mounted() {
    const url = 'https://jsonplaceholder.typicode.com/posts'
    axios.get(url).then(response => {
      this.posts = response.data
    }).catch(err => {
      return err
    })
  }
}
</script>