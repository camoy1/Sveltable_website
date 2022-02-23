<script>
  import Adam from '../assets/adam.svg';
	import Brad from '../assets/brad.svg';
	import Caryn from '../assets/care.svg';
	import Tom from '../assets/tommy.svg';
	import Mimi from '../assets/mimi.svg';
	let innerWidth;
	$: style = innerWidth > 800 ? 'desktop' : 'mobile';
</script>

<svelte:window bind:innerWidth />

<div class="SectionContainer">
	<div class="HeaderTitle">
		<h1>meet our team</h1>
	</div>

	<div class="CardSection">
		<!-- 
      Card for each person => Two columns (1:3 sizing) => Profile column (Photo div, Details div) and Bio column
    -->

		<!-- Adam Card -->
		<div class={`Card-${style}`}>
			<!-- Profile Column with Photo Section and Profile Details -->
			<div class={`ProfileColumn-${style}`}>
				<!-- Photo Section -->
				<div class={`PhotoSection-${style}`}>
          <img src={Adam} alt="Adam Moore" />
        </div>
				<!-- Profile Details, includling name and location -->
				<div class="ProfileDetails">
					<div class="ProfileText">
						<h4>Adam Moore</h4>
						<span><em>Tampa, Florida</em></span>
					</div>
					<!-- Personal Links for Icon -->
					<div class="Links">
						<a class="Icon" href="https://github.com/moore76sc" target="_blank">
							<div class="git">
								<i class="fab fa-github fa-2x" />
							</div>
						</a>
						<a
							class="Icon"
							href="https://www.linkedin.com/in/adam-moore-se/"
							target="_blank"
						>
							<div class="linkedin">
								<i class={`fab fa-linkedin fa-2x`} />
							</div>
						</a>
					</div>
				</div>
			</div>

			<!-- Bio Column -->
			<div class={`BioColumn-${style}`}>
				<span
					>Adam is a dedicated software engineer who is a hands-on leader that is skilled in
					coordinating functional teams in fast-paced environments. He participates in several
					outreach programs for children that are victims of child abuse and introduces many to
					computer programming. While he has served the community in various capacities, he now aims
					to serve through technology.
					<br /><i>“Development that makes a difference.”</i>
				</span>
			</div>
		</div>

		<!-- Brad Card -->
		<div class={`Card-${style}`}>
			<!-- Profile Column with Photo Section and Profile Details -->
			<div class={`ProfileColumn-${style}`}>
				<!-- Photo Section -->
				<div class={`PhotoSection-${style}`}>
          <img src={Brad} alt="Braddon Murphy" />
        </div>
				<!-- Profile Details, includling name and location -->
				<div class="ProfileDetails">
					<div class="ProfileText">
						<h4>Braddon Murphy</h4>
						<span><em>New York City, New York</em></span>
					</div>
					<!-- Personal Links for Icon -->
					<div class="Links">
						<a class="Icon" href="https://github.com/BraddonLee" target="_blank">
							<div class="git">
								<i class="fab fa-github fa-2x" />
							</div>
						</a>
						<a
							class="Icon"
							href="https://www.linkedin.com/in/braddonlee/"
							target="_blank"
						>
							<div class="linkedin">
								<i class={`fab fa-linkedin fa-2x`} />
							</div>
						</a>
					</div>
				</div>
			</div>

			<!-- Bio Column -->
			<div class={`BioColumn-${style}`}>
				<span>
					Braddon is a Full Stack software engineer who enjoys writing clean and reactive code, while always focusing on an excellent UX for end users. He will also beat you down a mountain on a pair of skis - apologies in advance.
				</span>
			</div>
		</div>

		<!-- Caryn Card -->
		<div class={`Card-${style}`}>
			<!-- Profile Column with Photo Section and Profile Details -->
			<div class={`ProfileColumn-${style}`}>
				<!-- Photo Section -->
				<div class={`PhotoSection-${style}`}>
          <img src={Caryn} alt="Caryn Moy" />
        </div>
				<!-- Profile Details, includling name and location -->
				<div class="ProfileDetails">
					<div class="ProfileText">
						<h4>Caryn Moy</h4>
						<span><em>she/her/hers</em></span>
						<br><span><em>Chicago, Illinois</em></span>
					</div>
					<!-- Personal Links for Icon -->
					<div class="Links">
						<a class="Icon" href="https://github.com/camoy1" target="_blank">
							<div class="git">
								<i class="fab fa-github fa-2x" />
							</div>
						</a>
						<a
							class="Icon"
							href="https://www.linkedin.com/in/caryn-moy/"
							target="_blank"
						>
							<div class="linkedin">
								<i class={`fab fa-linkedin fa-2x`} />
							</div>
						</a>
					</div>
				</div>
			</div>

			<!-- Bio Column -->
			<div class={`BioColumn-${style}`}>
				<span>
					Caryn is an empathetic software engineer who values quality mentorship and disability advocacy. When this Chicago-native is not coding or rock-climbing, she is creating social media content, producing podcast episodes, and organizing a scholarship and mutual aid grant for <a href="https://www.slpsofcolor.org/" target="_blank">Speech-Language Pathologists (SLPs) of Color</a> – a grassroots non-profit organization. She is dedicated to breaking down barriers for minoritized individuals in speech pathology, and now in tech! 
				</span>
			</div>
		</div>
    
		<!-- Mimi Card -->
		<div class={`Card-${style}`}>
			<!-- Profile Column with Photo Section and Profile Details -->
			<div class={`ProfileColumn-${style}`}>
				<!-- Photo Section -->
				<div class={`PhotoSection-${style}`}>
          <img src={Mimi} alt="Mimi Kwayo" />
        </div>
				<!-- Profile Details, includling name and location -->
				<div class="ProfileDetails">
					<div class="ProfileText">
						<h4>Mimi Kwayo</h4>
						<span><em>Houston, Texas</em></span>
					</div>
					<!-- Personal Links for Icon -->
					<div class="Links">
						<a class="Icon" href="https://github.com/TheMimStack" target="_blank">
							<div class="git">
								<i class="fab fa-github fa-2x" />
							</div>
						</a>
						<a
							class="Icon"
							href="https://www.linkedin.com/in/mimi-kwayo-587312226/ "
							target="_blank"
						>
							<div class="linkedin">
								<i class={`fab fa-linkedin fa-2x`} />
							</div>
						</a>
					</div>
				</div>
			</div>

			<!-- Bio Column -->
			<div class={`BioColumn-${style}`}>
				<span>
					Mimi is a Software Engineer based out of Houston, TX who enjoys building applications that make life easier. When she's not coding or hiking or traveling, she's eradicating dangerous beings, one spider at a time.
				</span>
			</div>
		</div>
    
		<!-- Tommy Card -->
		<div class={`Card-${style}`}>
			<!-- Profile Column with Photo Section and Profile Details -->
			<div class={`ProfileColumn-${style}`}>
				<!-- Photo Section -->
				<div class={`PhotoSection-${style}`}>
          <img src={Tom} alt="Tommy Ngo" />
        </div>
				<!-- Profile Details, includling name and location -->
				<div class="ProfileDetails">
					<div class="ProfileText">
						<h4>Tommy Ngo</h4>
						<span><em>Dallas, Texas</em></span>
					</div>
					<!-- Personal Links for Icon -->
					<div class="Links">
						<a class="Icon" href="https://github.com/tommmyngo" target="_blank">
							<div class="git">
								<i class="fab fa-github fa-2x" />
							</div>
						</a>
						<a
							class="Icon"
							href="https://www.linkedin.com/in/tommyhoaingo/"
							target="_blank"
						>
							<div class="linkedin">
								<i class={`fab fa-linkedin fa-2x`} />
							</div>
						</a>
					</div>
				</div>
			</div>

			<!-- Bio Column -->
			<div class={`BioColumn-${style}`}>
				<span>
					tommy bio
				</span>
			</div>
		</div>
	</div>
</div>

<style>
	a {
		color: black;
	}

	h4 {
		margin: 0.1rem 0 0.1rem 0;
    font-family: 'IBM Plex Sans', sans-serif;
	}
  
  em {
    font-family: 'IBM Plex Sans', sans-serif;
    font-weight: lighter;
    font-size: 0.8rem;
  }

	.PhotoSection-desktop {
		display: flex;
		justify-content: center;
		align-items: center;
    margin: 0.2rem 0 0.2rem 0;
	}

  .PhotoSection-mobile {
		display: flex;
		justify-content: center;
    margin: 0.2rem 0 0.2rem 0;
	}
  
  img {
		width: 80%;
		justify-self: center;
  }

	.SectionContainer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		padding: 4rem 0 4rem 0;
	}

	.HeaderTitle {
		color: #e6e6e6;
		font-family: 'IBM Plex Sans', sans-serif;
		display: flex;
		justify-content: center;
	}

	/* make responive */
	.CardSection {
		display: flex;
		flex-direction: column;
	}

	.Card-desktop {
		display: grid;
		border-radius: 10px;
		grid-template-columns: [left] 20% [right] 70%;
		align-items: center;
		justify-content: center;
		width: 50rem;
		min-height: 10rem;
		margin: 1rem 1rem 1rem 1rem;
		background-color: rgb(207, 207, 207);
	}

	.Card-mobile {
		width: 80vw;
		display: flex;
		border-radius: 10px;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		justify-items: center;
		margin: 1rem 1rem 1rem 1rem;
		background-color: rgb(207, 207, 207);
	}

	.ProfileColumn-desktop {
		display: flex;
		flex-direction: column;
		justify-content: center;
    margin: 1rem 0 1rem 0;
	}

  .ProfileColumn-mobile {
		display: flex;
		flex-direction: column;
    margin: 1rem 0 1rem 0;
	}

	.ProfileDetails {
		align-items: center;
		justify-content: center;
    margin: 0.5rem 0 0.5rem 0;
	}

	.ProfileText {
		justify-content: center;
		text-align: center;
	}

	.Links {
		display: flex;
		align-items: center;
		justify-content: center;
		margin-top: 0.5rem;
	}

	.Icon {
		margin: 0 0.5rem 0 0.5rem;
	}

	.BioColumn-desktop {
		display: flex;
		flex-direction: row;
		margin: 2rem 1rem 2rem 1rem;
    text-align: justify;
		text-justify: inter-word;
		font-family: 'IBM Plex Sans', sans-serif;
    font-weight: lighter;
    line-height: 1.3rem;
	}

	.BioColumn-mobile {
    display: flex;
    margin: 0 1rem 1rem 1rem; 
		font-family: 'IBM Plex Sans', sans-serif;
    font-weight: lighter;
    line-height: 1.3rem;
	}

	.BioColumn-mobile span {
		/* determine font style */
		text-align: center;
	}

	.git {
		color: #333; /* dark when header is light*/
	}

	.linkedin {
		color: #0077b5; /* linkedin blue directly from website when header is light */
	}
</style>
