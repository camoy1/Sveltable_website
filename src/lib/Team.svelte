<script>
  let innerWidth;
  $: style = innerWidth > 1000 ? 'desktop' : 'mobile'
</script>

<svelte:window bind:innerWidth={innerWidth}/>

<div class="SectionContainer" >
  <div class="HeaderTitle">
		<h2>meet our team</h2>
	</div>

  <div class="CardsContainer">
    <div class={`CardsContainer-top-${style}`}>
      <div class="Card">
        <div class="PIC">
          ADAM PIC
        </div>
        <div class="NAME">
          Adam Moore
        </div>
        <div class="BIO">
          BIO
        </div>
        <div class="LINKS">
          LIHNKS
        </div>
      </div>
      <div class="Card">
        <div class="PIC">
          BRAD PIC
        </div>
        <div class="NAME">
          Braddon Murphy
        </div>
        <div class="BIO">
          BIO
        </div>
        <div class="LINKS">
          LIHNKS
        </div>
      </div>
  
      <div class="Card">
        <div class="PIC">
          CARE PIC
        </div>
        <div class="NAME">
          Caryn Moy
        </div>
        <div class="BIO">
          BIO
        </div>
        <div class="LINKS">
          LIHNKS
        </div>
      </div>
    </div>
    <div class={`CardsContainer-bottom-${style}`}>
      <div class="Card">
        <div class="PictureContainer">
          MK
        </div>
        <div class="NAME">
          Mimi Kwayo
        </div>
        <div class="BIO">
          BIO
        </div>
        <div class="LINKS">
          LIHNKS
        </div>
      </div>
  
      <div class="Card">
        <div class="PictureContainer">
          TOMMY PIC
        </div>
        <div class="NAME">
          Tommy Ngo
        </div>
        <div class="BIO">
          BIO
        </div>
        <div class="LINKS">
          LIHNKS
        </div>
      </div>
    </div>
  </div>
</div>


<style>
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
  .CardsContainer{
    display: flex;
    flex-direction: column;
  }

  .CardsContainer-top-desktop, .CardsContainer-bottom-desktop {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
  }
  .CardsContainer-top-mobile, .CardsContainer-bottom-mobile {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
  }
  
  .Card {
    display: flex;
    border-radius: 25px;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 300px;
    height: 300px;
    margin: 1rem 1rem 1rem 1rem;
    background-color: rgb(207, 207, 207);
  }
</style>