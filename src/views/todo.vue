<template>
   <h1>Kegiatan Harian Yang Di Lakukan</h1>
	<div id="app">
		<form>
			<input type="text" v-model="newActivity" placeholder="Tambahkan kegiatan baru">
			<button type="submit" v-on:click.prevent="addActivity">Tambahkan</button>
		</form>
		<ul>
			<li v-for="(activity, index) in activities" :key="index" :class="{ completed: activity.completed }">
				{{ activity.name }}
				<button v-if="!activity.completed" v-on:click.prevent="completeActivity(index)">Selesai</button>
				<button v-on:click.prevent="removeActivity(index)">Hapus</button>
			</li>
		</ul>
		<div>
			<label><input type="checkbox" v-model="showCompleted"> Tampilkan hanya kegiatan yang belum selesai</label>
		</div>
	</div>
  </template>
  
  <script>
 export default {
  data() {
    return {
      newActivity: '',
      activities: [
        { name: 'Bermain Game', completed: false },
        { name: 'Olahraga', completed: true },
        { name: 'Belajar Java Script', completed: false }
      ],
      showCompleted: false
    };
  },
  methods: {
    addActivity() {
      if (this.newActivity.trim() !== '') {
        this.activities.push({
          name: this.newActivity.trim(),
          completed: false
        });
        this.newActivity = '';
      }
    },
    removeActivity(index) {
      this.activities.splice(index, 1);
    },
    completeActivity(index) {
      this.activities[index].completed = true;
    }
  },
  computed: {
    filteredActivities() {
      if (this.showCompleted) {
        return this.activities.filter(activity => !activity.completed);
      } else {
        return this.activities;
      }
    }
  }
};
  </script>
  
  <style scoped>
  #app {
  margin: 0 auto;
  max-width: 600px;
  padding: 20px;
  font-family: Arial, sans-serif;
}

h1 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 30px;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

li {
  margin-bottom: 10px;
  padding: 10px;
  border-radius: 5px;
  background-color: #f9f9f9;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li.completed {
  text-decoration: line-through;
}

button {
  background-color: #4CAF50;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #000300;
}

input[type="text"] {
  padding: 10px;
  border: none;
  border-radius: 5px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
  margin-right: 10px;
  flex-grow: 1;
}

label {
  display: block;
  margin-top: 20px;
}

input[type="checkbox"] {
  margin-right: 10px;
}

/* Styles for small devices */
@media only screen and (max-width: 600px) {
  ul {
    padding-left: 20px;
  }
  li {
    font-size: 16px;
  }
  input[type="text"], button[type="submit"] {
    width: 80%;
    padding: 10px;
    margin: 10px 0;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
}

/* Styles for medium devices */
@media only screen and (min-width: 601px) and (max-width: 900px) {
  ul {
    padding-left: 40px;
  }
  li {
    font-size: 18px;
  }
}

/* Styles for large devices */
@media only screen and (min-width: 901px) {
  ul {
    padding-left: 60px;
  }
  li {
    font-size: 20px;
  }
}


  
  </style>
  
  