<template>
  <div id="Current Bets">
    <p text-align="center">Current Bets</p>
    <b-table striped hover
            :items="items"
            :sort-desc="desc"
            :sort-by="sortBy"
            :fields="fields"/>
  </div>
</template>
<script>
import axios from 'axios';
export default {
  data () {
    return {
      sortBy: 'dom_points',
      desc: true,
      fields: [
        { key: 'initiator', sortable: true },
        { key: 'receiver', sortable: true },
        { key: 'description', sortable: false },
        { key: 'dom_points', sortable: true }
      ],
      items: [],
      errors: []
    }
  },
  created() {
  axios.get(`https://dompoints.herokuapp.com/api/bets/current/`)
    .then(response => {
      // JSON responses are automatically parsed.
      this.items = response.data
    })
    .catch(e => {
      this.errors.push(e)
    })

    // async / await version (created() becomes async created())

    //try {
    //  const response = await axios.get(`http://localhost:5000/api/test/`)
    //  this.posts = response.data
    //} catch (e) {
    //  this.errors.push(e)
    //}
  }
}
</script>
