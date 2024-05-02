<script>
  import { Topics, Speakers, Pricing } from '../lib/data.js';
  import TopicItem from '$lib/components/TopicItem.svelte';
  import Speaker from '$lib/components/Speaker.svelte';
  import Title from '$lib/components/Title.svelte';
  import TimelineItem from '$lib/components/TimelineItem.svelte'; 
  import ArrowDown from '$lib/assets/ArrowDown.svelte';
  import Layout from './+layout.svelte';
</script>

<div class="relative min-h-screen font-medium w-full flex flex-col xl:flex-row">
  <div
    class="z-10 flex-1 bg-gradient-to-b from-[#009EA8]/80 to-[#003844] to-80% xl:bg-gradient-to-tr xl:from-[#003844] xl:to-[#009EA8] text-white px-5 xl:pl-24 xl:pr-12 py-3 flex flex-col items-center xl:items-start xl:justify-between xl:w-3/5"
  >
    <div class="py-6 flex-1 xl:flex-none">
      <img src="meta2-white.svg" class="h-16 xl:h-24" alt="" />
    </div>
    <div class="flex flex-col">
      <div class="flex m-auto xl:m-0">
        <div
          class="xl:text-lg font-medium border-2 border-white px-4 py-1 xl:px-5 xl:py-2 rounded-full"
        >
          Call for paper
        </div>
      </div>
      <div
        class="mt-4 xl:mt-6 text-2xl xl:text-4xl text-center xl:text-left font-semibold leading-tight"
      >
        1st International Conference on Medical Technology and Its Application 2024
      </div>
    </div>
    <div
      class="mt-4 xl:mt-0 xl:flex items-center justify-between border-t border-white/35 pt-3 xl:pt-8 pb-12 w-full"
    >
      <div>
        <div class="text-lg xl:text-2xl font-light text-center xl:text-left">
          <span class="font-bold">16-17</span> October 2024
        </div>
        <div class="text-sm xl:text-base text-center xl:text-left font-light">
          JW Marriot Hotel Surabaya, East Java, Indonesia
        </div>
        <div
          class="text-center xl:text-left text-sm font-light tracking-wider underline opacity-80"
        >
          See important dates
        </div>
      </div>
      <div>
        <a
          href="#more"
          class="bg-white rounded-full px-6 py-2 h-12 xl:h-14 xl:text-lg text-teal-950 flex justify-between items-center mt-16 xl:mt-0"
        >
          More Info
          <div class="size-5 xl:size-6 xl:ml-5">
            <ArrowDown />
          </div>
        </a>
      </div>
    </div>
  </div>
  <div class="z-0 absolute xl:static bg-black inset-y-0 xl:w-2/5">
    <img src="foto-gedung-fkk-min.jpg" class="object-cover h-full" alt="" />
  </div>
</div>

<div id="more" class="container mx-auto px-5 py-16 xl:py-32 flex flex-col items-center">
  <div class="text-2xl xl:text-4xl text-gradient-meta font-medium max-w-4xl text-center">
    “Recent Breakthroughs in Medical Technology and Healthcare System”
  </div>
  <div class="max-w-4xl text-center mt-8 xl:mt-12 xl:text-lg text-gray-600">
    META 2024 is the annual international conference held by the Department of Electrical
    Engineering of the Institut Teknologi Sepuluh Nopember (ITS), Surabaya, Indonesia. It was
    previously known as SITIA and has been held annually by the department since 1999. This year,
    META will be held in hybrid.
  </div>
  <div class="max-w-4xl text-center mt-3 xl:mt-5 xl:text-lg text-gray-600">
    Papers that are accepted and presented at META 2024 will be submitted for possible inclusion
    in IEEE Xplore, subject to meeting IEEE Xplore’s scope and quality requirements. If an author
    fails to register for the conference or does not present their paper, the paper will be flagged
    as a ‘no show’ and removed from the conference proceedings.
  </div>

  <Title title="Important Dates" />
  <div class="px-5 xl:px-0 mt-5 xl:mt-12 mx-auto xl:w-5/6 grid xl:grid-cols-6">
    <TimelineItem id="1" date="1 May 2024" description="Paper Submission Page Open" />
    <TimelineItem id="2" date="29 June 2024" description="Paper Submission Due" />
    <TimelineItem id="3" date="1 July 2024" description="Acceptance Notification" />
    <TimelineItem id="4" date="16 August 2024" description="Final Manuscript Submission" />
    <TimelineItem id="5" date="16 September 2024" description="Regsitration Due" />
    <TimelineItem id="6" date="10 October 2024" description="Video Presentation Due" />
  </div>

  <Title title="Topics of Interests" />
  <div class="xl:w-4/5 mt-12 grid xl:grid-cols-3 gap-2 xl:gap-3">
    {#each Topics as topic}
      <TopicItem data={topic} />
    {/each}
  </div>
</div>

<div id="keynote-speaker" class="px-5 xl:px-0 bg-gradient-meta">
  <div class="xl:w-3/5 mx-auto py-16 xl:py-32">
    <div class="text-3xl xl:text-4xl font-medium text-white text-center">Keynote Speaker</div>
    <div class="divide-y divide-white/25">
      {#each Speakers as speaker}
        <Speaker data={speaker} />
      {/each}
    </div>
  </div>
</div>

<Title title="Registration" />

<div class="px-5 xl:px-0 mt-5 xl:mt-12 xl:w-3/5 mx-auto">
  <div class="text-lg xl:text-2xl text-gradient-meta font-medium mb-2 xl:mb-3">
    Registration Payment Method
  </div>
  <div>
    Online registration along with the receipt of transferred fee, as an attachment Registration
    will be confirmed only when the registration fee (non-refundable) has been paid.  Please note
    that author and/or additional paper registrations are non-refundable.
  </div>

  <div class="mt-5 xl:mt-12 rounded-lg ring-1 ring-gray-200 overflow-hidden">
    <div class=" flex text-white bg-gradient-meta text-sm xl:text-base font-medium tracking-wide">
      <div class="p-3 flex-1">Category</div>
      <div class="p-3 w-[123px] text-center border-x border-white/20">International</div>
      <div class="p-3 w-32 xl:w-40 text-center">Domestik</div>
    </div>
    <div class="divide-y">
      {#each Pricing as price}
        <div class="flex text-sm xl:text-base hover:bg-gray-100">
          <div class="flex-1 px-2 py-1 xl:p-3 font-medium">{price.category}</div>
          <div class="flex items-center justify-end px-2 py-1 xl:p-3 w-[123px] border-x">
            {price.international}
          </div>
          <div class="flex items-center justify-end px-2 py-1 xl:p-3 w-32 xl:w-40 text-right">
            {price.domestic}
          </div>
        </div>
      {/each}
    </div>
  </div>

  <div class="xl:grid xl:grid-cols-2 divide-y xl:divide-y-0 xl:divide-x mt-5 xl:mt-8">
    <div class="xl:pr-6 mb-5">
      <div class="text-lg xl:text-2xl mb-3 font-medium text-gradient-meta">
        International Participants
      </div>
      <div>
        Registration payments for international participants are made via EDAS using a credit card
        at an exchange rate of US dollars. Confirmation is automatic because it uses the EDAS
        system. If your payment is successful, the status will change to PAID.
      </div>
      <a
        href="https://edas.info/r31248"
        class="rounded-full px-6 py-1 mt-6 ring-1 hover:ring-2 ring-[#009EA8] inline-block text-gradient-meta text-sm xl:text-base font-medium transform duration-150"
        >Click here</a
      >
    </div>
    <div class="xl:pl-8 pt-5 xl:pt-0">
      <div class="text-lg xl:text-2xl mb-3 font-medium text-gradient-meta">
        Domestic Participants
      </div>
      <div>
        Registration Payment for Domestic Participants can be made by local bank transfer, to:
        <ul class="list-disc px-6 my-3">
          <li>Name of Bank: <strong>Bank BNI</strong></li>
          <li>Beneficiary Name: <strong>Teknologi Kedokteran</strong></li>
          <li>Virtual Account number: <strong>988 111 335 921 0000</strong></li>
        </ul>
        To make it easier to check, please add the last 3 digits of your id paper to the registration
        fee. Confirmation is manual, meaning you must inform and send proof of transfer at this link
        below:
      </div>
      <a
        href="https://edas.info/r31248"
        class="rounded-full px-6 py-1 mt-6 ring-1 hover:ring-2 ring-[#009EA8] inline-block text-gradient-meta text-sm xl:text-base font-medium transform duration-150"
        >Click here</a
      >
    </div>
  </div>
</div>

<Title title="Submissions" />

<div class="px-5 xl:px-0 mt-5 xl:mt-12 xl:w-3/5 mx-auto">
  <div class="text-lg xl:text-2xl text-gradient-meta font-medium mb-2 xl:mb-3">
    Paper Submission
  </div>
  <div>
    <ul class="list-disc px-6 my-3">
      <li>
        Please submit your paper through the EDAS conference management system through the following
        link: https://edas.info/N31869.
      </li>
      <li>Papers should follow the two-column IEEE conference style, between 4 to 6 pages.</li>
      <li>
        Please consult the following link for manuscript templates:
        https://www.ieee.org/conferences/publishing/templates.html
      </li>
      <li><strong>Final manuscript should be in paper size of A4 (A4 template)</strong></li>
    </ul>
  </div>

  <div class="text-lg xl:text-2xl text-gradient-meta font-medium mb-2 xl:mt-5">
    Final Manuscript Preparation
  </div>
  <div>
    <ul class="list-decimal px-6 my-3">
      <li>
        You must revise your manuscript according to the comments and suggestions given by the
        reviewers.
      </li>
      <li>Ensure that you have added all the author names, both in your manuscript and in EDAS.</li>
      <li>
        You are required to ensure that the similarity rating of your manuscript is less than 30%.
      </li>
      <li>
        Submissions with a similarity rating of 30% or above will be dropped and no longer
        considered for META 2024.
      </li>
      <li>
        Please ensure that your manuscript has been checked for grammatical and typographical
        errors, and that your manuscript is IEEE PDF eXpress compliant.
        <ul class="list-disc px-6">
          <li>
            A formatting checklist is given here to help you prepare your manuscript before
            uploading it to IEEE PDF eXpress.
          </li>
          <li>
            You should also upload the confirmed checklist during the registration process. The
            details on how to use IEEE pdf eXpress to generate your PDF file can be found here.
          </li>
        </ul>
      </li>
      <li>
        You are required to transfer the copyright of the manuscript to IEEE if you wish your
        manuscript to be published.
      </li>
      <li>This can be done electronically through EDAS.</li>
      <li>
        IEEE reserves the right to exclude a paper from distribution after the conference (e.g.,
        removal from IEEE Xplore) if the paper is not presented at the conference.
      </li>
    </ul>
  </div>

  <div class="text-lg xl:text-2xl text-gradient-meta font-medium mb-2 xl:mt-5">
    IEEE PDF eXpress Guidelines
  </div>
  <div>
    <ul class="list-disc px-6 my-3">
      <li>IEEE’s PDF eXpress for META 2024 will open at Site Open Date: Conference ID: (TBA)</li>
      <li>Make sure your manuscript has been revised.</li>
      <li>Visit the website of IEEE PDF eXpress at https://ieee-pdf-express.org/</li>
      <li>
        First time users should do the following:
        <ul class="list-decimal px-6 my-3">
          <li>Select the New Users – Click here link.</li>
          <li>
            Enter the following:
            <ul class="list-disc px-6 my-3">
              <li>(Conference ID will be announced later)</li>
              <li>Your email address</li>
              <li>A password</li>
            </ul>
          </li>
          <li>
            Continue to enter information as prompted. Verify that your contact information is
            valid.
          </li>
        </ul>
      </li>
      <li>
        Previous users of PDF eXpress need to follow the same steps above, but should enter the same
        password that was used for the previous conferences.
      </li>
      <li>
        For each paper ID that is created,IEEE PDF eXpress is able to convert up to 20 source files
        and perform checking of 10 PDF files.
      </li>
      <li>For more details, visit https://ieee-pdf-express.org/External/UsingIEEEPDFeXpress</li>
    </ul>
  </div>
</div>

<Title title="Venue" />

<div class="container mt-8 xl:mt-12 mx-auto px-5 xl:px-0 xl:w-3/5 xl:space-x-8 xl:flex">
  <div class="xl:w-1/2 mt-5 xl:mt-0">
    <div class="text-xl xl:text-2xl font-medium leading-tight">JW Marriott Hotel Surabaya</div>
    <div class="xl:text-lg mt-2 leading-tight opacity-75">
      Jl. Embong Malang No.85-89, Kedungdoro, Kec. Tegalsari, Surabaya, Jawa Timur 60261
    </div>
  </div>
  <div class="relative w-full xl:w-1/2 h-40 xl:h-80 rounded-xl overflow-hidden">
    <iframe
      class="absolute top-0 left-0 w-full h-full"
      src="https://maps.google.com/maps?q=jw+marriot+hotel+surabaya&t=&z=14&ie=UTF8&iwloc=&output=embed"
      frameborder="0"
      title="JW Marriot Tunjungan Surabaya"
    ></iframe>
  </div>
</div>

<Title title="Organizing Committee" />
<div class="container mt-8 xl:mt-12 mx-auto px-5 xl:px-0 xl:w-4/5 xl:space-x-8 xl:flex">
  <div class="mt-5 xl:mt-0 mx-auto space-y-1">
    <div class="flex items-center space-x-3">
      <div class="xl:w-52 xl:text-lg font-medium">General Chair</div>
      <div class="xl:text-lg opacity-75">: Fahmi Mubarok, S.T., M.Sc., Ph.D. (ITS)</div>
    </div>

    <div class="flex items-center space-x-3">
      <div class="xl:w-52 xl:text-lg font-medium">Technical Program Chair</div>
      <div class="xl:text-lg opacity-75">: Dr. Shoffi Izza Sabilla, S.Kom. (ITS)</div>
    </div>

    <div class="flex items-center space-x-3">
      <div class="xl:w-52 xl:text-lg font-medium">Publication Chair</div>
      <div class="xl:text-lg opacity-75">: Dr. Dhany Arifianto, S.T., M.Eng., Ph.D. (ITS)</div>
    </div>

    <div class="flex items-center space-x-3">
      <div class="xl:w-52 xl:text-lg font-medium">Secretary</div>
      <div class="xl:text-lg opacity-75">: dr. Putri Alief Siswanto, M.T. (ITS)</div>
    </div>

    <div class="flex items-center space-x-3">
      <div class="xl:w-52 xl:text-lg font-medium">Treasurer</div>
      <div class="xl:text-lg opacity-75">: Achmad Syaifuddin, S.T., M..Eng., Ph..D. (ITS)</div>
    </div>
  </div>
</div>

<Title title="Contact" />

<div
  class="container mt-8 mb-12 xl:mt-12 xl:mb-32 mx-auto px-5 xl:px-0 xl:w-4/5 xl:space-x-8 xl:flex"
>
  <div class="xl:w-3/5 flex flex-col items-center text-center mx-auto justify-between">
    <div class="space-y-3">
      <div class="text-xl xl:text-2xl font-medium leading-tight">
        Institut Teknologi Sepuluh Nopember Surabaya<br />East Java, Indonesia
      </div>
      <div class="xl:text-lg leading-tight opacity-75">
        Jl. Raya ITS Sukolilo<br />
        Gedung Fakultas Kedokteran dan Kesehatan Lantai 2,<br />
        Keputih, Sukolilo, Surabaya, East Java 60111
      </div>
      <div class="space-y-2 xl:space-x-1 mt-3">
        <a
          href="mailto:meta@its.ac.id"
          class="rounded-full px-3 py-1 xl:px-5 xl:py-2 ring-1 hover:ring-2 ring-black inline-block xl:text-lg transform duration-150"
          >Email: <span class="font-medium underline">meta@its.ac.id</span></a
        >
        <a
          href="https://wa.me/628112811240"
          class="rounded-full px-3 py-1 xl:px-5 xl:py-2 ring-1 hover:ring-2 ring-black inline-block xl:text-lg transform duration-150"
          >WhatsApp: <span class="font-medium underline">62 8112-8112-40</span> (Mr. Fahmi Mubarok)</a
        >
      </div>
    </div>
  </div>
</div>
