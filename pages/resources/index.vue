<template>
  <article>
    <SocialHead :title="title" :description="description" :image="image" />
    <link href="https://unpkg.com/pattern.css" rel="stylesheet" />
    <div>
      <section>
        <div class="max-w-6xl mx-auto px-5 py-5 ">
          <div class="text-center mb-20">
            <h1
              class="main-heading title-font  mb-4 text-4xl font-extrabold leading-10 tracking-tight sm:text-5xl sm:leading-none md:text-6xl"
            >
              My Resources
            </h1>
            <p class="text-base leading-relaxed xl:w-2/4 lg:w-3/4 mx-auto">
              Here is a list of my resources which include podcasts I have been
              a guest on. Live Streams, interviews, blog posts that have
              featrued me and so much more.
            </p>
            <div class="flex mt-6 justify-center">
              <div
                class="w-16 h-1 rounded-full bg-indigo-500 inline-flex"
              ></div>
            </div>
          </div>
          <div class="flex flex-wrap sm:-m-4 -mx-4 -mb-10 -mt-4 ">
            <div
              v-for="resource in resources"
              :key="resource.title"
              class="p-10 md:w-1/3 md:mb-0 mb-6 flex flex-col "
            >
              <ResourcesCard :resource="resource" />
            </div>
          </div>
        </div>
      </section>
    </div>
  </article>
</template>
<script>
  export default {
    async asyncData({ $content }) {
      const resources = await $content('resources')
        .sortBy('position')
        .fetch()

      return {
        resources
      }
    },
    data() {
      return {
        title: "Debbie's list of resources from podcasts to videos to posts",
        description:
          'A list of resources I have written, created, appeared in, talked about and more',
        image:
          'https://res.cloudinary.com/debsobrien/image/upload/v1607284331/debbie.codes/Screenshot_2020-12-06_at_20.51.40_hvbwkd.png'
      }
    },
    head() {
      return {
        title: this.title,
        meta: [
          {
            hid: 'description',
            name: 'desctiption',
            content: this.desctiption
          }
        ],
        link: [
          { rel: 'stylesheet', href: 'https://unpkg.com/pattern.css' },
          {
            hid: 'canonical',
            rel: 'canonical',
            href: `https://debbie.codes/resources/${this.$route.params.slug}`
          }
        ]
      }
    }
  }
</script>
