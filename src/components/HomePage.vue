<template>
    <div>
		<div class="header-content">
			<h2>get ahead</h2>
			<div class="container">
				<div class="upper-group">
					<HeaderTile>
						<img src="../assets/Contacts@3x.svg">
						<h4>Make New Contacts</h4>
						<p>Thecosystems is all about people. Not data.</p>
					</HeaderTile>
					<HeaderTile>
						<img src="../assets/Decisions.png">
						<h4>Make Better Decisions</h4>
						<p>Understand your stakeholders and their needs.</p>
					</HeaderTile>
					<HeaderTile>
						<img src="../assets/Time.png">
						<h4>Stay Up to Date</h4>
						<p>Things change quickly.</p>
					</HeaderTile>
				</div>
				<div class="lower-group">
					<HeaderTile>
						<img src="../assets/Network.png">
						<h4>Explore Professional Networks</h4>
						<p>Understand your stakeholders and their needs.</p>
					</HeaderTile>
					<HeaderTile>
						<img src="../assets/Perspective.png">
						<h4>Identify Hidden Opportunities</h4>
						<p>Open a new world of possibility and engagement.</p>
					</HeaderTile>
				</div>
			</div>
		</div>
		<div class="body-content">
			<div class="container">
				<div class="text-block block1">
					<h3>available now</h3>
					<h1>No waiting, start today</h1>
					<p>Traditional stakeholder mapping takes time – usually months. If we have a Thecosystem in the area you’re working in, you can have it today.</p>
				</div>
				<div class="text-block block2">
					<h3>global</h3>
					<h1>Expertise does not need a passport.</h1>
					<p>Brilliance, drive, and influence can emerge anywhere in the world. A system subscription gives you a global view of the real movers and shakers.</p>
				</div>
				<div class="text-block block3">
					<h3>clear-cut</h3>
					<h1>No big databases to navigate.</h1>
					<p>When looking for a needle in a haystack, why go digging around in a bigger haystack? Each system focuses on one therapeutic condition at a time, so you can focus on what matters.</p>
				</div>
				<div class="text-block block4">
					<h3>subscription</h3>
					<h1>Affordable</h1>
					<p>3-, 6-, and 12-month subscriptions instantly available.</p>
				</div>
			</div>
		</div>
    </div>
</template>

<script>
import { gsap } from 'gsap';
import {ScrollTrigger} from 'gsap/ScrollTrigger';
import HeaderTile from '../components/HeaderTile';

gsap.registerPlugin(ScrollTrigger);


export default {
  name: 'HomePage',

  components: {
	HeaderTile,
    },

	// Animate each block in as it is scrolled past the center of the page
	mounted: function () {
		gsap.to('.block1', {
			duration:2,
			autoAlpha: 1,
			stagger: 2,
			ease: "slow.out(1.7)",
			delay: 0.2,
			scrollTrigger: {
			trigger: '.block1',
			start: 'top center',
			end: () => `+=${document.querySelector('.block1').offsetHeight}`,
			toggleActions: 'play reverse play reverse',
			// onEnter, onLeave, onEnterBack, onLeaveBack
			}
	}),
	gsap.to('.block2', {
			duration:2,
			autoAlpha: 1,
			stagger: 2,
			ease: "slow.out(1.7)",
			delay: 0.2,
			scrollTrigger: {
			trigger: '.block2',
			start: 'top center',
			end: () => `+=${document.querySelector('.block2').offsetHeight}`,
			toggleActions: 'play reverse play reverse',
			// onEnter, onLeave, onEnterBack, onLeaveBack
			}
	}),
	gsap.to('.block3', {
			duration:1,
			autoAlpha: 1,
			stagger: 1,
			ease: "slow.out(1.7)",
			delay: 0.2,
			scrollTrigger: {
			trigger: '.block3',
			start: 'top center',
			end: () => `+=${document.querySelector('.block3').offsetHeight}`,
			toggleActions: 'play reverse play reverse',
			// onEnter, onLeave, onEnterBack, onLeaveBack
			}
	}),
	gsap.to('.block4', {
			duration:1,
			autoAlpha: 1,
			stagger: 1,
			ease: "slow.out(1.7)",
			delay: 0.2,
			scrollTrigger: {
			trigger: '.block4',
			start: 'top center',
			end: () => `+=${document.querySelector('.block4').offsetHeight}`,
			toggleActions: 'play reverse play reverse',
			// onEnter, onLeave, onEnterBack, onLeaveBack
			}
	})
	},
}
</script>


<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Lato');
@import '../assets/styles.scss';
</style>
