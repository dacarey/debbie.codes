<template>
  <div class="flex flex-col mt-20 px-4 py-6">
    <ColorModePicker />
    <footer class="text-center mt-8">
      <p class="mb-4">
        © Debbie O'Brien, Palma de Mallorca, Spain
      </p>
      <ul class="flex justify-center">
        <li class="mx-2">
          <a href="https://twitter.com/debs_obrien" aria-label="twitter">
            <IconTwitter class="h-10 w-10 fill-current" />
          </a>
        </li>
        <li class="mx-2">
          <a
            href="https://www.linkedin.com/in/debbie-o-brien-1a199975/"
            aria-label="linkedIn"
          >
            <IconLinkedIn class="h-10 w-10 fill-current" />
          </a>
        </li>
        <li class="mx-2">
          <a
            href="https://www.youtube.com/channel/UCrNvYFsT1L3WczE8AizDQ6g/"
            aria-label="youtube"
          >
            <IconYouTube class="h-10 w-10 fill-current" />
          </a>
        </li>
        <li class="mx-2">
          <a href="https://github.com/debs-obrien" aria-label="github">
            <IconGithub class="h-10 w-10 fill-current" />
          </a>
        </li>
        <li class="mx-2">
          <a href="https://noti.st/debbie" aria-label="speaker profile">
            <IconSpeaker class="h-10 w-10 fill-current" />
          </a>
        </li>

        <li class="mx-2">
          <a href="mailto:debbie@nuxtjs.com" aria-label="eamil">
            <IconEmail class="h-10 w-10 fill-current" />
          </a>
        </li>
        <li class="mx-2">
          <a
            href="https://www.buymeacoffee.com/debbieobrien"
            aria-label="buy me a coffee"
          >
            <IconCoffee class="h-10 w-10 fill-current" />
          </a>
        </li>
      </ul>
    </footer>
    <CookieBox />
  </div>
</template>
<script>
  import IconEmail from '@/assets/icons/email.svg?inline'
  import IconGithub from '@/assets/icons/github.svg?inline'
  import IconTwitter from '@/assets/icons/twitter.svg?inline'
  import IconLinkedIn from '@/assets/icons/linkedIn.svg?inline'
  import IconYouTube from '@/assets/icons/youtube.svg?inline'
  import IconSpeaker from '@/assets/icons/speaker.svg?inline'
  import IconCoffee from '@/assets/icons/coffee.svg?inline'
  export default {
    components: {
      IconEmail,
      IconGithub,
      IconTwitter,
      IconLinkedIn,
      IconYouTube,
      IconSpeaker,
      IconCoffee
    }
  }
</script>

<style scoped></style>
