<script>
import Categories from '@/components/Categories.vue';
import Footer from '@/components/Footer.vue';
import Pagination from '@/components/Pagination.vue';
import Post from '@/components/Post.vue';
import PostFilter from '@/components/PostFilter.vue';
import RecentPost from '@/components/RecentPost.vue';
import UserList from '@/components/UserList.vue';

export default {
  components: {
    PostFilter,
    Pagination,
    Footer,
    UserList,
    Categories,
    RecentPost,
    Post
  },
  data() {
    return {
      posts: [
        {
          id: 1,
          date: "Jun 1, 2020",
          tag: "Laravel",
          title: "Build Your New Idea with Laravel Freamwork.",
          body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tempora expedita dicta totam aspernatur doloremque. Excepturi iste iusto eos enim reprehenderit nisi, accusamus delectus nihil quis facere in modi ratione libero!",
          image: "https://images.unsplash.com/photo-1492562080023-ab3db95bfbce?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=731&q=80",
          userName: "Alex John"
        },
        {
          id: 2,
          date: "mar 4, 2019",
          tag: "Design",
          title: "Accessibility tools for designers and developers",
          body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tempora expedita dicta totam aspernatur doloremque. Excepturi iste iusto eos enim reprehenderit nisi, accusamus delectus nihil quis facere in modi ratione libero!",
          image: "https://images.unsplash.com/photo-1464863979621-258859e62245?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=333&q=80",
          userName: "Jane Doe"
        },
      ]
    }
  }
}
</script>

<template>
  <div class="px-6 py-8">
    <div class="flex justify-between container mx-auto">
      <div class="w-full lg:w-8/12">
        <div class="flex items-center justify-between">
          <h1 class="text-xl font-bold text-gray-700 md:text-2xl">Post</h1>
          <PostFilter />
        </div>
        <div class="mt-6" v-for="post in posts" :key="post.id">
          <Post :data="post"></Post>
        </div>
        <div class="mt-8">
          <Pagination />
        </div>
      </div>
      <div class="-mx-8 w-4/12 hidden lg:block">
        <div class="px-8">
          <h1 class="mb-4 text-xl font-bold text-gray-700">Authors</h1>
          <UserList />
        </div>
        <div class="mt-10 px-8">
          <h1 class="mb-4 text-xl font-bold text-gray-700">Categories</h1>
          <Categories />
        </div>
        <div class="mt-10 px-8">
          <h1 class="mb-4 text-xl font-bold text-gray-700">Recent Post</h1>
          <RecentPost />
        </div>
      </div>
    </div>
  </div>

  <Footer />
</template>
