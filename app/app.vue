<script setup lang="ts">
const heroImages = [
  {
    src: '/images/hero-1.jpeg',
    alt: 'Suikerterrein image 1',
    caption: 'Field research at Suikerterrein'
  },
  {
    src: '/images/hero-2.jpeg',
    alt: 'Suikerterrein image 2',
    caption: 'Artist community and temporary spaces'
  },
  {
    src: '/images/hero-3.jpeg',
    alt: 'Suikerterrein image 3',
    caption: 'Traces of cultural production'
  },
  {
    src: '/images/hero-4.jpeg',
    alt: 'Suikerterrein image 4',
    caption: 'Industrial traces and everyday use'
  },
  {
    src: '/images/hero-5.jpeg',
    alt: 'Suikerterrein image 5',
    caption: 'Temporary cultural space in transition'
  },
  {
    src: '/images/hero-6.jpeg',
    alt: 'Suikerterrein image 6',
    caption: 'Field observation around the site'
  },
  {
    src: '/images/hero-7.jpeg',
    alt: 'Suikerterrein image 7',
    caption: 'Archive fragments from Suikerterrein'
  },
  {
    src: '/images/hero-8.jpeg',
    alt: 'Suikerterrein image 8',
    caption: 'Artistic community and urban change'
  },
  {
    src: '/images/hero-9.jpeg',
    alt: 'Suikerterrein image 9',
    caption: 'Built fragments and shared working spaces'
  },
  {
    src: '/images/hero-10.jpeg',
    alt: 'Suikerterrein image 10',
    caption: 'Everyday materials inside the terrain'
  },
  {
    src: '/images/hero-11.jpeg',
    alt: 'Suikerterrein image 11',
    caption: 'Studios, workshops, and temporary structures'
  },
  {
    src: '/images/hero-12.jpeg',
    alt: 'Suikerterrein image 12',
    caption: 'Post-industrial space in active use'
  },
  {
    src: '/images/hero-13.jpeg',
    alt: 'Suikerterrein image 13',
    caption: 'Artist spaces shaped by time and reuse'
  }
]

const navItems = [
  { label: 'Introduction', href: '#introduction' },
  { label: 'About Suikerterrein', href: '#about' },
  { label: 'Interviews', href: '#interviews' },
  { label: 'Team', href: '#team' },
  { label: 'Contact', href: '#contact' }
]

const aboutSections = [
  {
    title: 'About the Site',
    text: 'Suikerterrein is part of Groningen’s former sugar factory site. Once connected to the city’s industrial production, the area has gradually been reused after the factory closed. In recent years, it has developed into a mixed and transitional urban space that includes events, food, education, workshops, creative practices, and a wide range of users.'
  },
  {
    title: 'Why It Matters',
    text: 'The specificity of Suikerterrein lies in the fact that it is neither a fully planned new district nor simply a preserved industrial site. It remains a place in transition. Temporary use, open-ended development, and future urban redevelopment overlap here, making it an important case for observing how cities change.'
  },
  {
    title: 'Why We Study It',
    text: 'For our artist research, Suikerterrein is not only about which artists work here. We are interested in how artistic practice becomes embedded in a changing environment. Artist communities, event spaces, and other users together shape the site’s current cultural, spatial, and social condition.'
  }
]

const interviews = [
  {
    name: 'Roeksrariteiten',
    label: 'Maruschka & Laurens / wonder / nature',
    image: '/images/interview-maruschka-laurens.jpeg',
    object: 'Nettle plant',
    audio: '/audio/maruschka-laurens.mp3',
    website: {
      label: 'roeksrariteiten.nl',
      url: 'https://roeksrariteiten.nl'
    },
    quote: 'Something that is rejected can actually be essential.',
    summary: 'Maruschka and Laurens work together through drawing, wonder, practical making, and a shared interest in reconnecting humans with nature.',
    profiles: [
      {
        name: 'Maruschka',
        text: 'Maruschka has been drawing all her life. During her time at art academy, it became clear to her that what you create can have an impact on people. It does not necessarily have to be art; it should evoke a sense of wonder. One of the most essential themes today, in her view, is reconnecting humans with nature.'
      },
      {
        name: 'Laurens',
        text: 'Laurens provides practical support. If he does not yet know how to do something, he learns it. From digital work to hands-on making and construction, he applies a wide range of skills to transform a good idea into a great one, especially when working with Maruschka\'s drawings.'
      }
    ],
    themes: ['Ecosystem', 'Weeds', 'Fairytale stories'],
    fragments: [
      {
        title: 'Not every cluster is a community',
        text: 'Suikerterrein looks like a community from the outside, but Maruschka and Laurens describe something more fragile. People work near each other, share the same terrain, and sometimes help one another, yet proximity alone does not create a collective life.\n\nFor them, a real community begins when people build something together. It needs trust, exchange, and a shared direction. At Suikerterrein, these things appear in small moments: a neighbor helping with welding, a workshop opening its doors, a collaboration growing through personal contact.\n\nBut the site is also full of invisible fences. Some people protect their own territory. Some groups remain separate islands. The community here is not one unified body, but a loose ecology of connections, distances, and small negotiations.'
      },
      {
        title: 'Low rent as survival',
        text: 'For Maruschka and Laurens, Suikerterrein matters first because it made survival possible. After art school, artistic life was not sustained by inspiration alone. It depended on rent, time, tools, and the ability to stop working too many unrelated jobs.\n\nThe low rent allowed them to build a practice without immediately turning everything into profit. Instead of spending most of their income on space, they could put it back into their work.\n\nThis changes the meaning of the terrain. It is not only a place to work. It is a condition that allows artists to keep going, to experiment, and to grow slowly before the outside world demands financial certainty.'
      },
      {
        title: 'The nettle as a social model',
        text: 'Maruschka and Laurens chose the nettle as a symbol for Suikerterrein. A nettle is often treated as a weed, something unwanted or messy. But in an ecosystem, it is essential. Many butterflies depend on it. Without nettles, other forms of life disappear.\n\nThis image becomes a way to understand artist spaces like Suikerterrein. They may look temporary, rough, or inconvenient from the perspective of urban planning. Yet they support practices, relationships, and ways of living that cannot easily exist in polished commercial spaces.\n\nThe nettle shows their central idea: what a city rejects may be exactly what keeps its cultural ecosystem alive.'
      }
    ]
  },
  {
    name: 'Robert Paul Sprenkeling',
    label: 'Stained glass / self-built studio',
    image: '/images/interview-robert.jpeg',
    object: 'A photograph of colored glass',
    audio: '/audio/robert.mp3',
    website: {
      label: 'glasinloodgroningen.nl',
      url: 'https://www.glasinloodgroningen.nl/'
    },
    quote: 'We use the area with the uncertainty of life.',
    summary: 'Robert Paul Sprenkeling is a stained glass artist and founder of Glas in Lood Groningen, a self-built glass workshop on Suikerterrein. His practice combines craft, reuse, teaching, and commissioned stained glass work.',
    profiles: [],
    themes: ['Light', 'Colors', 'Uncertainty'],
    fragments: [
      {
        title: 'Building from what already had a life',
        text: 'Robert did not enter a finished studio. He arrived at a piece of concrete land and had to imagine the building himself. Containers became walls. Roof plates became shelter. Reused wood, old windows, found materials, and other people’s skills slowly turned an empty plot into a working place.\n\nMost of the studio was built from second-hand materials. Some came from the internet, some from demolished sites, some through conversations, and some through coincidence. Robert is drawn to materials that already carry a past.\n\nBecause of this, his studio is not only functional. It feels assembled from different histories. The building holds labor, reuse, memory, and the decision to make something beautiful out of what was available.'
      },
      {
        title: 'The certainty of leaving',
        text: 'Robert knows that Suikerterrein may end around 2030. He does not treat this as a surprise. For him, the deadline has always been part of the agreement: the land is temporary, the buildings may have to move, and nothing here is fully owned.\n\nBut this uncertainty does not make the place meaningless. Robert does not want to spend years worrying before the moment arrives. He accepts that some things need to be secure, such as shelter, health, and the next practical step. Beyond that, the future can remain open.\n\nHis view changes the way Suikerterrein is understood. Temporary does not mean unimportant. It means the value of the place exists in the time, energy, and life that people place into it while it is here.'
      },
      {
        title: 'Stepping stones in the city',
        text: 'Robert sees Suikerterrein as part of a wider network of temporary cultural spaces in Groningen. These places appear in empty buildings, forgotten corners, or areas waiting for redevelopment. They give people room to work, meet, dance, learn, and briefly step outside the normal rhythm of the city.\n\nOften, people only recognize their value when they are about to disappear. Visitors come and say that such places should stay forever. But Robert suggests that their temporary nature may also be what keeps them alive, flexible, and open.\n\nFor him, the question is not only how to save Suikerterrein. The bigger question is whether the city can keep making room for new temporary spaces to emerge when old ones vanish.'
      }
    ]
  },
  {
    name: 'Floris Maathuis',
    label: 'Creative explorations in technology',
    image: '/images/interview-floris.jpeg',
    object: 'Reused building materials',
    audio: '/audio/floris.mp3',
    website: {
      label: 'florismaathuis.nl',
      url: 'https://www.florismaathuis.nl'
    },
    quote: 'Almost everything here has a story.',
    summary: 'Floris Maathuis brings technology and creativity together into tailor-made solutions and innovations. Working with businesses, governments, social and cultural organizations, and many other clients, he develops creative technological approaches for social issues, communication, product innovation, and entertainment.',
    profiles: [],
    themes: ['Community', 'Creativity', 'Ecosystem'],
    fragments: [
      {
        title: 'From sugar factory to temporary initiatives',
        text: 'Floris begins with the site’s industrial past. Suikerterrein was once part of a large sugar factory, connected to canals, processing fields, and the production of sugar from beets. The area was shaped by work, infrastructure, and heavy industry long before artists arrived.\n\nAfter the factory disappeared, the city allowed the land to be used for temporary initiatives. This created a rare opening: a large piece of urban space that was not yet fully controlled by housing plans, commercial development, or fixed architecture.\n\nIn that gap, artists and makers entered. What used to be a factory terrain became a place for studios, workshops, experiments, and self-built structures. The site moved from industrial production to cultural production.'
      },
      {
        title: 'A club of makers',
        text: 'Floris describes the group as a kind of club or association. People became members, contributed money, crowdfunded, borrowed from friends and family, searched for materials, and built the place together.\n\nNothing arrived ready-made. A beach house became a workspace. A garden shed was taken apart and rebuilt. Containers became structures. Old military units, ship containers, salvaged wood, and second-hand parts found new functions.\n\nThis makes the terrain feel like a collective construction rather than a designed campus. Almost everything has a story. The buildings show not only what people needed, but also how they solved problems together with limited resources.'
      },
      {
        title: 'What survives after 2030',
        text: 'Floris knows that the future of Suikerterrein is uncertain. Housing development is already moving closer, and the current use of the terrain is expected to end around 2030. People are now organizing, discussing, and lobbying the city to see whether parts of what grew here can remain.\n\nBut the real question is not only whether the buildings survive. The deeper question is whether the conditions survive: affordable space, shared responsibility, freedom to build, access to materials, and time for creative practices to develop slowly.\n\nIf Suikerterrein disappears, the physical site may be cleared. But what matters is whether the city understands what was produced here: not only objects or events, but a way of making space together.'
      }
    ]
  }
]

const teamMembers = [
  {
    name: 'Yize Huang',
    role: 'Researcher / Artist',
    image: '/images/team-yize.jpg',
    bio: 'I am from Taipei, Taiwan. My practice often begins with the body, vulnerability, memory, and states of survival. I am interested in how people maintain their form under pressure, isolation, or unstable conditions, and how emotions that cannot be fully articulated leave traces through objects, text, and space. In my work, sculpture is not only an object, but also a body that continues to stand after being wounded. These sculptures may appear broken, tilted, or fragile, yet they remain placed within a space. Through damaged materials, repetition, and accumulation, I try to present a state of being unable to truly fall down: not because of strength, but because some people do not have the privilege to collapse.',
    reflection: 'This field research focuses on Suikerterrein, a former industrial site that has gradually become a place where art, events, and urban life intersect. Its transformation reminds me of similar spaces in Taiwan, such as old factories, warehouses, abandoned buildings, and marginal areas that have been reused by artists and communities. I am interested in how artistic ecosystems emerge in these places: why artists gather there, how they use or change the space, and how the space influences them. Through Suikerterrein, I hope to observe the relationship between artists, the city, and the changing life of a place.'
  },
  {
    name: 'YuTzu Hsu',
    role: 'Interdisciplinary Artist / Researcher',
    image: '/images/team-yuzu.png',
    bio: 'She is an interdisciplinary artist whose work often begins with observations of human culture, everyday life, and rituals. Through performance, collective making, and interventions, she explores how relationships between people are formed within specific situations.',
    reflection: 'Her practice often takes the form of artistic interventions and collective creation, focusing on experiences in everyday life that are difficult to articulate. She explores how bodily memory shapes personal histories and habitual rituals, and how interactions between people influence one another and contribute to the formation of cultural environments. Working with groups and the body as a medium, she tries to transform personal memory into situations that can be experienced and participated in by others, allowing relationships between individuals and collectives to emerge and shift.'
  },
  {
    name: 'Ayeen Fazel',
    role: 'Artist-facilitator / Researcher',
    image: '/images/team-Ayeen.jpeg',
    bio: 'Ayeen Fazel is an artist-facilitator based in Groningen, working at the intersection of installation, storytelling, and participatory practice. Her work focuses on creating spaces where people can explore questions of belonging, land, and human connection through shared experiences. Drawing from personal and collective research, she works with translucent materials, shadow, and text to construct environments where viewers become part of the work. Her practice is rooted in facilitation, inviting reflection through simple yet fundamental questions rather than fixed answers.',
    reflection: 'I’m very interested in this area because I find it amazing and different from other places in the city. I was curious about what is happening here, the history behind it, how this place became what it is today, and who the people are. I already had some information, but after talking with the artists, I gained a much clearer vision, along with different perspectives. What I found especially interesting is how they built something temporary, but at the same time created something that goes beyond that: an approach and way of living that can continue even after this place is gone.'
  },
  {
    name: 'Leila Mokhtari',
    role: 'Visual Artist / Ceramic Artist / Researcher',
    image: '/images/team-leila.png',
    bio: 'I was born in 1994 in Iran, and for almost ten years my main practice has been in the field of visual art and functional ceramics. My academic background is in sculpture, and most of the artworks I create are three-dimensional. Space is the most fundamental element of my projects, and it can fully represent my thoughts.',
    reflection: 'As I began working, I became interested in the concept of history and the passing of time, and I try to distinguish its connection with our contemporary world. I am also inspired by ancient architecture, literature, and their bonds with the human soul. While my main career is related to fine art, I launched a ceramic studio a couple of years ago, and a major part of my practice has focused on developing a pottery studio, learning how to collaborate, and making progress through shared work.'
  },
  {
    name: 'Shiva Miryektah',
    role: 'Painter / Researcher',
    image: '/images/team-shiva.jpeg',
    bio: 'In my recent painting project, I use references to Iranian architectural geometry, tilework, and mirror structures to study adaptive visual sequences through return, shift, absence, fracture, and reconfiguration. Through this, I visually explore how coexistence can be imagined as a balance between autonomy and a shared condition: each work remains independent while responding to one recurring structural logic that connects the series without making it uniform.',
    reflection: 'I joined this project to extend this question into the context of the Suikerterrein, a temporary artistic community in a former industrial site. I am interested in how artists create continuity within a place whose current cultural use is being reshaped by planned redevelopment, shaped by presence, adaptation, and a shared environment. In conversations with the participating artists, I explore how this community contributes to the cultural memory of the site, leaving traces of presence, practice, and belonging that are not always officially preserved or visibly acknowledged.'
  }
]

const contactPeople = [
  {
    name: 'YuTzu',
    email: 'harleyhsu1997@gmail.com',
    phone: '+31 619120184'
  },
  {
    name: 'Ayeen',
    email: 'fazel.ayeen@gmail.com',
    phone: '+31 657415641'
  }
]

const currentHeroIndex = ref(0)
const activeProfileIndexes = ref<Record<string, number>>({})
let heroInterval: ReturnType<typeof setInterval> | undefined

const currentHeroImage = computed(() => heroImages[currentHeroIndex.value])

const selectHeroImage = (index: number) => {
  currentHeroIndex.value = index
}

const getActiveProfileIndex = (name: string) => activeProfileIndexes.value[name] ?? 0

const selectProfile = (name: string, index: number) => {
  activeProfileIndexes.value = {
    ...activeProfileIndexes.value,
    [name]: index
  }
}

onMounted(() => {
  heroInterval = setInterval(() => {
    currentHeroIndex.value = (currentHeroIndex.value + 1) % heroImages.length
  }, 5000)
})

onBeforeUnmount(() => {
  if (heroInterval) {
    clearInterval(heroInterval)
  }
})
</script>

<template>
  <main class="min-h-screen bg-stone-50 text-xl text-neutral-900 antialiased sm:text-2xl">
    <section class="border-b border-neutral-300 bg-stone-100">
      <div class="mx-auto max-w-7xl px-4 py-5 sm:px-6 lg:px-8">
        <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
          Artist research / Field archive / Groningen
        </p>
      </div>

      <div class="mx-auto max-w-7xl px-4 pb-8 sm:px-6 lg:px-8">
        <div class="relative overflow-hidden border border-neutral-300 bg-neutral-200">
          <Transition name="fade" mode="out-in">
            <img
              :key="currentHeroImage.src"
              :src="currentHeroImage.src"
              :alt="currentHeroImage.alt"
              class="aspect-[16/10] w-full object-cover grayscale-[20%] sm:aspect-auto sm:h-[68vh] sm:min-h-[360px]"
            >
          </Transition>
        </div>

        <div class="mt-4 border-b border-neutral-300 pb-6">
          <div>
            <h1 class="max-w-4xl text-6xl font-normal leading-tight text-neutral-950 sm:text-7xl lg:text-9xl">
              Suikerterrein
            </h1>
            <p class="mt-4 max-w-3xl text-2xl leading-9 text-neutral-700 sm:text-3xl">
              {{ currentHeroImage.caption }}
            </p>
          </div>

          <div class="mt-8 overflow-x-auto">
            <div class="flex w-max gap-3 pb-3">
              <button
                v-for="(image, index) in heroImages"
                :key="image.src"
                type="button"
                class="group shrink-0 border bg-stone-50 p-1 transition duration-200"
                :class="currentHeroIndex === index ? 'border-neutral-950' : 'border-neutral-300 opacity-60 hover:border-neutral-600 hover:opacity-100'"
                :aria-label="`Show ${image.alt}`"
                @click="selectHeroImage(index)"
              >
                <img
                  :src="image.src"
                  :alt="image.alt"
                  class="h-20 w-28 object-cover grayscale transition duration-200 group-hover:grayscale-0 sm:w-32"
                  :class="currentHeroIndex === index ? 'grayscale-0' : ''"
                >
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <nav class="sticky top-0 z-20 border-b border-neutral-300 bg-stone-50/95 backdrop-blur">
      <div class="mx-auto max-w-7xl overflow-x-auto px-4 sm:px-6 lg:px-8">
        <div class="flex min-w-max items-center gap-8 py-5 text-lg uppercase tracking-[0.14em] text-neutral-600">
          <a
            v-for="item in navItems"
            :key="item.href"
            :href="item.href"
            class="whitespace-nowrap transition duration-200 hover:text-neutral-950"
          >
            {{ item.label }}
          </a>
        </div>
      </div>
    </nav>

    <section id="introduction" class="scroll-mt-24 border-b border-neutral-300">
      <div class="mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 md:grid-cols-[0.8fr_1.2fr] lg:px-8 lg:py-28">
        <div>
          <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
            Introduction
          </p>
          <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
            Artist Research: Suikerterrein
          </h2>
        </div>

        <div class="max-w-4xl text-2xl leading-10 text-neutral-700">
          <p>
            This website presents an artist research project about Suikerterrein, an artist and cultural community in Groningen that is expected to disappear around 2030 due to future redevelopment. Through interviews, we investigated how artists experience this place, how they build community, and what may be lost when such temporary cultural spaces are removed.
          </p>
        </div>
      </div>
    </section>

    <section class="border-b border-neutral-300 bg-[#ede8df]">
      <div class="mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 md:grid-cols-[0.8fr_1.2fr] lg:px-8 lg:py-28">
        <div>
          <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
            Research ground
          </p>
          <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
            Motivation
          </h2>
        </div>

        <div class="max-w-4xl text-2xl leading-10 text-neutral-700">
          <p>
            Our motivation comes from a concern for temporary artist communities and the fragile spaces that support them. Suikerterrein is not only a physical location, but also a living network of artists, makers, events, memories, and informal support. By interviewing people connected to the site, we want to understand what this place means before it changes or disappears.
          </p>
        </div>
      </div>
    </section>

    <section id="about" class="scroll-mt-24 border-b border-neutral-300">
      <div class="mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 md:grid-cols-[0.8fr_1.2fr] lg:px-8 lg:py-28">
        <div>
          <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
            Site notes
          </p>
          <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
            About Suikerterrein
          </h2>
          <p class="mt-5 max-w-md text-xl leading-8 text-neutral-600">
            A compact archive of context, temporary use, future redevelopment, and the cultural questions around the site.
          </p>
        </div>

        <div class="grid max-w-4xl gap-9">
          <article
            v-for="section in aboutSections"
            :key="section.title"
            class="border-t border-neutral-300 pt-6"
          >
            <h3 class="text-3xl font-normal leading-tight text-neutral-950 sm:text-4xl">
              {{ section.title }}
            </h3>
            <p class="mt-4 text-2xl leading-10 text-neutral-700">
              {{ section.text }}
            </p>
          </article>
        </div>
      </div>
    </section>

    <section id="interviews" class="scroll-mt-24 border-b border-neutral-300 bg-[#23312d] text-stone-50">
      <div class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8 lg:py-28">
        <div class="grid gap-8 md:grid-cols-[0.8fr_1.2fr]">
          <div>
            <p class="text-base uppercase tracking-[0.22em] text-stone-400">
              Oral archive
            </p>
            <h2 class="mt-4 text-5xl font-normal leading-tight sm:text-6xl">
              Interviews
            </h2>
          </div>

          <p class="max-w-4xl text-2xl leading-10 text-stone-300">
            Three conversations trace Suikerterrein through self-built studios, informal support, ecological thinking, temporary land use, and the question of what may remain after 2030.
          </p>
        </div>

        <div class="mt-14 grid gap-10 lg:grid-cols-[0.34fr_0.66fr]">
          <aside class="border-t border-stone-500 pt-6 lg:sticky lg:top-28 lg:self-start">
            <p class="text-base uppercase tracking-[0.22em] text-stone-400">
              Interviewees
            </p>
            <div class="mt-6 grid gap-5">
              <a
                v-for="interview in interviews"
                :key="interview.name"
                :href="`#interview-${interview.name.toLowerCase().replaceAll(' ', '-').replaceAll('&', 'and')}`"
                class="group border-l border-stone-500 pl-5 transition duration-200 hover:border-stone-100"
              >
                <span class="block text-2xl leading-tight text-stone-100">
                  {{ interview.name }}
                </span>
                <span class="mt-2 block text-base leading-6 text-stone-400 group-hover:text-stone-300">
                  {{ interview.label }}
                </span>
              </a>
            </div>
          </aside>

          <div class="grid gap-8">
            <article
              v-for="interview in interviews"
              :id="`interview-${interview.name.toLowerCase().replaceAll(' ', '-').replaceAll('&', 'and')}`"
              :key="interview.name"
              class="scroll-mt-32 border border-stone-600 bg-[#1f2a27]"
            >
              <div class="grid">
                <img
                  :src="interview.image"
                  :alt="`${interview.name} interview material`"
                  class="aspect-[16/9] w-full object-cover grayscale-[20%]"
                >

                <div class="grid gap-8 p-6 sm:p-8 lg:grid-cols-[0.38fr_0.62fr]">
                  <div>
                    <p class="text-base uppercase tracking-[0.18em] text-stone-400">
                      {{ interview.label }}
                    </p>
                    <h3 class="mt-3 text-4xl font-normal leading-tight text-stone-50 sm:text-5xl">
                      {{ interview.name }}
                    </h3>

                    <blockquote class="mt-7 border-l border-stone-300 pl-5 text-2xl italic leading-9 text-stone-100">
                      "{{ interview.quote }}"
                    </blockquote>
                  </div>

                  <div>
                    <p class="text-lg leading-8 text-stone-200 sm:text-xl">
                      {{ interview.summary }}
                    </p>

                    <div
                      v-if="interview.profiles.length"
                      class="mt-7 border-t border-stone-600 pt-5"
                    >
                      <div class="grid grid-cols-2 gap-2">
                        <button
                          v-for="(profile, profileIndex) in interview.profiles"
                          :key="profile.name"
                          type="button"
                          class="min-h-12 border px-4 py-3 text-left text-base leading-6 transition duration-200"
                          :class="getActiveProfileIndex(interview.name) === profileIndex ? 'border-stone-100 bg-stone-100 text-[#1f2a27]' : 'border-stone-600 text-stone-300 hover:border-stone-300 hover:text-stone-100'"
                          @click="selectProfile(interview.name, profileIndex)"
                        >
                          {{ profile.name }}
                        </button>
                      </div>

                      <div class="mt-5 min-h-[14rem] border-l border-stone-500 pl-5">
                        <p class="text-lg leading-8 text-stone-100">
                          {{ interview.profiles[getActiveProfileIndex(interview.name)].text }}
                        </p>
                      </div>
                    </div>

                    <div class="mt-7 grid gap-4 border-t border-stone-600 pt-6 sm:grid-cols-2">
                      <div>
                        <p class="text-sm uppercase tracking-[0.18em] text-stone-400">
                          Offered object
                        </p>
                        <p class="mt-2 text-xl leading-7 text-stone-100">
                          {{ interview.object }}
                        </p>
                      </div>

                      <div>
                        <p class="text-sm uppercase tracking-[0.18em] text-stone-400">
                          Key themes
                        </p>
                        <div class="mt-3 flex flex-wrap gap-2">
                          <span
                            v-for="theme in interview.themes"
                            :key="theme"
                            class="border border-stone-500 px-3 py-1 text-base leading-6 text-stone-200"
                          >
                            {{ theme }}
                          </span>
                        </div>
                      </div>
                    </div>

                    <div class="mt-7 border-t border-stone-600 pt-6">
                      <p class="text-sm uppercase tracking-[0.18em] text-stone-400">
                        Recording
                      </p>
                      <audio class="mt-4 w-full" controls preload="none" :src="interview.audio" />
                    </div>

                    <div class="mt-7 border-t border-stone-600 pt-6">
                      <p class="text-sm uppercase tracking-[0.18em] text-stone-400">
                        Website
                      </p>
                      <a
                        :href="interview.website.url"
                        target="_blank"
                        rel="noreferrer"
                        class="mt-3 inline-flex border border-stone-500 px-3 py-2 text-base leading-6 text-stone-200 transition duration-200 hover:border-stone-200 hover:text-stone-50"
                      >
                        {{ interview.website.label }}
                      </a>
                    </div>
                  </div>
                </div>
              </div>

              <div class="border-t border-stone-600">
                <details
                  v-for="fragment in interview.fragments"
                  :key="fragment.title"
                  class="group border-b border-stone-700 last:border-b-0"
                >
                  <summary class="flex cursor-pointer list-none items-center justify-between gap-4 px-6 py-5 text-xl leading-7 text-stone-100 transition duration-200 hover:bg-stone-100/5 sm:px-8">
                    <span>{{ fragment.title }}</span>
                    <span class="text-2xl leading-none text-stone-400 transition duration-200 group-open:rotate-45">+</span>
                  </summary>
                  <p class="px-6 pb-7 text-xl leading-9 text-stone-300 sm:px-8">
                    {{ fragment.text }}
                  </p>
                </details>
              </div>
            </article>
          </div>
        </div>
      </div>
    </section>

    <section id="team" class="scroll-mt-24 border-b border-neutral-300 bg-stone-50 px-4 py-20 sm:px-6 lg:px-8 lg:py-28">
      <div class="mx-auto max-w-7xl">
        <div class="mb-12 max-w-3xl">
          <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
            Team
          </p>
          <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
            Researchers
          </h2>
          <p class="mt-6 text-xl leading-8 text-neutral-600">
            This research was developed by five members through interviews, field observation, and artistic reflection.
          </p>
        </div>

        <div class="grid gap-6">
          <article
            v-for="member in teamMembers"
            :key="member.name"
            class="grid overflow-hidden border border-neutral-300 bg-stone-100 lg:grid-cols-[18rem_1fr]"
          >
            <img
              :src="member.image"
              :alt="member.name"
              class="aspect-[4/5] w-full object-cover grayscale-[15%] lg:h-full"
            >

            <div class="p-6 sm:p-8">
              <p class="text-xs uppercase tracking-[0.24em] text-neutral-500">
                {{ member.role }}
              </p>

              <h3 class="mt-3 text-3xl font-medium text-neutral-900">
                {{ member.name }}
              </h3>

              <div class="mt-6 grid gap-6 xl:grid-cols-2">
                <div>
                  <p class="text-xs uppercase tracking-[0.2em] text-neutral-500">
                    Practice
                  </p>
                  <p class="mt-3 text-base leading-8 text-neutral-700">
                    {{ member.bio }}
                  </p>
                </div>

                <div class="border-t border-neutral-300 pt-5 xl:border-l xl:border-t-0 xl:pl-6 xl:pt-0">
                  <p class="text-xs uppercase tracking-[0.2em] text-neutral-500">
                    Project focus
                  </p>
                  <p class="mt-3 text-base leading-8 text-neutral-700">
                    {{ member.reflection }}
                  </p>
                </div>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="contact" class="scroll-mt-24 bg-[#f2efe8] px-4 py-16 text-neutral-900 sm:px-6 lg:px-8 lg:py-20">
      <div class="mx-auto max-w-7xl">
        <div class="grid gap-10 border-b border-neutral-300 pb-12 md:grid-cols-[0.7fr_1.3fr] md:items-end">
          <div>
            <p class="text-base uppercase tracking-[0.22em] text-neutral-500">
              Contact
            </p>
            <h2 class="mt-4 text-5xl font-normal leading-tight text-neutral-950 sm:text-6xl">
              Keep in touch
            </h2>
          </div>

          <p class="max-w-3xl text-xl leading-8 text-neutral-600 md:justify-self-end md:text-right">
            For questions about the research, interviews, or project material, please contact YuTzu or Ayeen.
          </p>
        </div>

        <div class="grid border-b border-neutral-300 md:grid-cols-2">
          <article
            v-for="person in contactPeople"
            :key="person.email"
            class="border-neutral-300 py-9 md:px-8 md:first:border-r md:first:pl-0 md:last:pr-0"
          >
            <div class="grid gap-8 sm:grid-cols-[0.45fr_1fr]">
              <h3 class="text-4xl font-normal leading-tight text-neutral-950 sm:text-5xl">
                {{ person.name }}
              </h3>

              <div class="grid gap-6">
                <div>
                  <p class="text-xs uppercase tracking-[0.2em] text-neutral-500">
                    Email
                  </p>
                  <a
                    :href="`mailto:${person.email}`"
                    class="mt-2 block break-words text-lg leading-7 text-neutral-700 transition duration-200 hover:text-neutral-950 sm:text-xl"
                  >
                    {{ person.email }}
                  </a>
                </div>

                <div>
                  <p class="text-xs uppercase tracking-[0.2em] text-neutral-500">
                    Phone
                  </p>
                  <a
                    :href="`tel:${person.phone.replaceAll(' ', '')}`"
                    class="mt-2 block text-lg leading-7 text-neutral-700 transition duration-200 hover:text-neutral-950 sm:text-xl"
                  >
                    {{ person.phone }}
                  </a>
                </div>
              </div>
            </div>
          </article>
        </div>

        <p class="pt-8 text-sm uppercase tracking-[0.2em] text-neutral-500">
          Suikerterrein artist research / Groningen
        </p>
      </div>
    </section>
  </main>
</template>
