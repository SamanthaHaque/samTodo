<template>
 
<div class="projects mx-2 " >
  <v-simple-table  class="simple-table">
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left description">
       Client Name
          </th>
             <th class="text-left description">
           Project Name
          </th>
          <th class="text-left description">
            Date
          </th>
              <th class="text-left description">
            Image
          </th>
          <th class="text-left description">
            Description
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in loadedMeetups"
          :key="item.Id"
        >
          <td class="" ><div class="d-flex">
            <div class="name-box">{{ item.title }} </div><div> <img :src= item.image style="width: 10px; height: 10px" /></div></div></td>
        <td class="description">{{ item.project }}</td>
          <td class="description">{{ item.date }}</td>
           <td class="description">  <img :src= item.imageUrl class="image" /></td>
             <td class="description">{{ item.description }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>

</div>

</template>

<script>
  export default {
    name: 'App',
    data () {
      return {
    loadedMeetups: [
      {
        id: "1",
        title: "Albert Ainstein" ,
         image: "https://cdn-icons-png.flaticon.com/512/1828/1828884.png",
         project:"Design a new website",
        imageUrl:
          "https://www.teahub.io/photos/full/119-1197715_format-hd-42nd-street-photo.jpg",
        date: "2009-07",
        description:
          "It is a long established fact that a reader will be distracted by ",
      },
      {
        id: "2",
        title: "John Smith",
       image: "https://cdn-icons-png.flaticon.com/512/1828/1828884.png",
       project:"Design video thumbnails",
        imageUrl:
          "https://live.staticflickr.com/8677/16643297922_714055b69c_b.jpg",
        date: "2019-11",
        description:
          "There are many variations of passages of Lorem Ipsum available, but the majmbined with a handful of model seIpsum is therefore always free from repetition, injected humour, or non-characteristic words etc.",
      },
      {
        id: "3",
        title: "Jessica Perker",
        image: "https://cdn-icons-png.flaticon.com/512/1828/1828884.png",
        project:"Code up the homepage",
           imageUrl:
          "https://www.teahub.io/photos/full/119-1197715_format-hd-42nd-street-photo.jpg",
        date: "2019-07",
        description:
          "There are many variatiovable. If ym Ipsum generators onuser non-characteristic words etc.",
      },
      {
        id: "4",
        title: "Tory Hills",
        image: "https://cdn-icons-png.flaticon.com/512/1828/1828884.png",
        imageUrl:
          "https://happyairtravel.com/wp-content/uploads/2019/10/Why-You-Should-Visit-Italy.jpg",
          project:"Create a community forum",
        date: "2017-07",
        description:
          'The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interesh versions from the 1914 translation by H. Rackham.',
      },
    ],
      }
    },
  }
</script>
<style scoped>

.simple-table{
  margin:  100px  30px 0 30px;
}
.simple-table tr{
  height: 50px !important;
}
td{
  height: 100px !important;
  text-overflow: ellipsis !important;
  overflow: hidden;
  padding: 5px;
}
th{
  padding: 10px;
}
th.description{
    max-width: 20vw;
  text-overflow: ellipsis !important;
  white-space: nowrap;
  overflow: hidden;
}
td.description{
  max-width: 20vw;
  text-overflow: ellipsis !important;
  white-space: nowrap;
  overflow: hidden;
}
td .name-box{
  max-width: 20vw;
  text-overflow: ellipsis !important;
  white-space: nowrap;
  overflow: hidden;
}
.image{
  width: 40px; height: 40px;
}
@media (max-width:480px) {
  td.description{
  max-width: 9vw !important;
  text-overflow: ellipsis !important;
  white-space: nowrap;
  overflow: hidden;
}
th.description{
    max-width: 9vw;
  text-overflow: ellipsis !important;
  white-space: nowrap;
  overflow: hidden;
}
  td .name-box{
  max-width: 10vw !important;
  text-overflow: ellipsis !important;
  white-space: nowrap;
  overflow: hidden;
}
th{
  padding: 0 !important;
}
.image{
  width: 30px; height: 30px;
}

}

</style>