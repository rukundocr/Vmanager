<template>

  <div class="add container">
   
    <router-link to="/">BACK</router-link>
    <hr>
    <h1 class="text-success">GLOBAL COVID-19 OUTBREAK STATISTICS</h1>
    <h3 class="text-warning">POSITVE CASES: <span class="badge badge-dark text-danger ">{{global.cases}} </span></h3>
    <h3 class="text-warning">TOTAL DEATHS: <span class="badge badge-danger">{{global.deaths}} </span></h3>
    <h3 class="text-warning">RECOVERED: <span class="badge badge-warning">{{global.recovered}} </span></h3>
    
      <h3 class="text-primary">Search by Country . Select Any Country to see current update  </h3>
      <h1 class="page-header text-success">Country:{{corona.country}}  ::: 
        Positive Cases: <span class="badge badge-primary">{{corona.cases}}
          </span> Deaths: <span class="badge badge-primary">
            {{corona.deaths}}</span></h1> 
       <h1 class="page-header text-danger">{{error}}</h1>
    <form v-on:submit="search" id="district">
    <label>SELECT COUNTRY</label>
   <select v-model="selected" class="form-control" placeholder="select a country">
   <option value="Afghanistan">Afghanistan</option>
   <option value="Albania">Albania</option>
   <option value="Algeria">Algeria</option>
   <option value="Andorra">Andorra</option>
   <option value="Angola">Angola</option>
   <option value="Anguilla">Anguilla</option>
   <option value="Antigua">Barbuda</option>
   <option value="Argentina">Argentina</option>
   <option value="Armenia">Armenia</option>
   <option value="Aruba">Aruba</option>
   <option value="Australia">Australia</option>
   <option value="Austria">Austria</option>
   <option value="Azerbaijan">Azerbaijan</option>
   <option value="Bahamas">Bahamas</option>
   <option value="Bahrain">Bahrain</option>
   <option value="Bangladesh">Bangladesh</option>
   <option value="Barbados">Barbados</option>
   <option value="Belarus">Belarus</option>
   <option value="Belgium">Belgium</option>
   <option value="Belize">Belize</option>
   <option value="Benin">Benin</option>
   <option value="Bermuda">Bermuda</option>
   <option value="Bhutan">Bhutan</option>
   <option value="Bolivia">Bolivia</option>
   <option value="Bonaire">Bonaire</option>
   <option value="Bosnia">Bosnia & Herzegovina</option>
   <option value="Botswana">Botswana</option>
   <option value="Brazil">Brazil</option>
   <option value="Brunei">Brunei</option>
   <option value="Bulgaria">Bulgaria</option>
   <option value="Burkina Faso">Burkina Faso</option>
   <option value="Burundi">Burundi</option>
   <option value="Cambodia">Cambodia</option>
   <option value="Cameroon">Cameroon</option>
   <option value="Canada">Canada</option>
   <option value="Chad">Chad</option>
   <option value="Chile">Chile</option>
   <option value="China">China</option>
   <option value="Colombia">Colombia</option>
   <option value="Comoros">Comoros</option>
   <option value="Congo">Congo</option>
   <option value="Cook Islands">Cook Islands</option>
   <option value="Costa Rica">Costa Rica</option>
   <option value="Ivory coast">Cote DIvoire</option>
   <option value="Croatia">Croatia</option>
   <option value="Cuba">Cuba</option>
   <option value="Curaco">Curacao</option>
   <option value="Cyprus">Cyprus</option>
   <option value="Czech Republic">Czech Republic</option>
   <option value="Denmark">Denmark</option>
   <option value="Djibouti">Djibouti</option>
   <option value="Dominica">Dominica</option>
   <option value="Dominican Republic">Dominican Republic</option>
   <option value="East Timor">East Timor</option>
   <option value="Ecuador">Ecuador</option>
   <option value="Egypt">Egypt</option>
   <option value="El Salvador">El Salvador</option>
   <option value="Equatorial Guinea">Equatorial Guinea</option>
   <option value="Eritrea">Eritrea</option>
   <option value="Estonia">Estonia</option>
   <option value="Ethiopia">Ethiopia</option>
   <option value="Fiji">Fiji</option>
   <option value="Finland">Finland</option>
   <option value="France">France</option>
   <option value="Gabon">Gabon</option>
   <option value="Gambia">Gambia</option>
   <option value="Georgia">Georgia</option>
   <option value="Germany">Germany</option>
   <option value="Ghana">Ghana</option>
   <option value="Gibraltar">Gibraltar</option>
   <option value="Greece">Greece</option>
   <option value="Greenland">Greenland</option>
   <option value="Grenada">Grenada</option>
   <option value="Guadeloupe">Guadeloupe</option>
   <option value="Guam">Guam</option>
   <option value="Guatemala">Guatemala</option>
   <option value="Guinea">Guinea</option>
   <option value="Guyana">Guyana</option>
   <option value="Haiti">Haiti</option>
   <option value="Hawaii">Hawaii</option>
   <option value="Honduras">Honduras</option>
   <option value="Hong Kong">Hong Kong</option>
   <option value="Hungary">Hungary</option>
   <option value="Iceland">Iceland</option>
   <option value="Indonesia">Indonesia</option>
   <option value="India">India</option>
   <option value="Iran">Iran</option>
   <option value="Iraq">Iraq</option>
   <option value="Ireland">Ireland</option>
   <option value="Isle of Man">Isle of Man</option>
   <option value="Israel">Israel</option>
   <option value="Italy">Italy</option>
   <option value="Jamaica">Jamaica</option>
   <option value="Japan">Japan</option>
   <option value="Jordan">Jordan</option>
   <option value="Kazakhstan">Kazakhstan</option>
   <option value="Kenya">Kenya</option>
   <option value="Kiribati">Kiribati</option>
   <option value="Korea ">Korea South</option>
   <option value="Kuwait">Kuwait</option>
   <option value="Kyrgyzstan">Kyrgyzstan</option>
   <option value="Laos">Laos</option>
   <option value="Latvia">Latvia</option>
   <option value="Lebanon">Lebanon</option>
   <option value="Lesotho">Lesotho</option>
   <option value="Liberia">Liberia</option>
   <option value="Libya">Libya</option>
   <option value="Liechtenstein">Liechtenstein</option>
   <option value="Lithuania">Lithuania</option>
   <option value="Luxembourg">Luxembourg</option>
   <option value="Macau">Macau</option>
   <option value="Macedonia">Macedonia</option>
   <option value="Madagascar">Madagascar</option>
   <option value="Malaysia">Malaysia</option>
   <option value="Malawi">Malawi</option>
   <option value="Maldives">Maldives</option>
   <option value="Mali">Mali</option>
   <option value="Malta">Malta</option>
   <option value="Martinique">Martinique</option>
   <option value="Mauritania">Mauritania</option>
   <option value="Mauritius">Mauritius</option>
   <option value="Mayotte">Mayotte</option>
   <option value="Mexico">Mexico</option>
   <option value="Moldova">Moldova</option>
   <option value="Monaco">Monaco</option>
   <option value="Mongolia">Mongolia</option>
   <option value="Montserrat">Montserrat</option>
   <option value="Morocco">Morocco</option>
   <option value="Mozambique">Mozambique</option>
   <option value="Myanmar">Myanmar</option>
   <option value="Nambia">Nambia</option>
   <option value="Nauru">Nauru</option>
   <option value="Nepal">Nepal</option>
   <option value="Netherlands">Netherlands (Holland, Europe)</option>
   <option value="Nevis">Nevis</option>
   <option value="New Caledonia">New Caledonia</option>
   <option value="New Zealand">New Zealand</option>
   <option value="Nicaragua">Nicaragua</option>
   <option value="Niger">Niger</option>
   <option value="Nigeria">Nigeria</option>
   <option value="Niue">Niue</option>
   <option value="Norway">Norway</option>
   <option value="Oman">Oman</option>
   <option value="Pakistan">Pakistan</option>
   <option value="Palau Island">Palau Island</option>
   <option value="Palestine">Palestine</option>
   <option value="Panama">Panama</option>
   <option value="Paraguay">Paraguay</option>
   <option value="Peru">Peru</option>
   <option value="Phillipines">Philippines</option>
   <option value="Poland">Poland</option>
   <option value="Portugal">Portugal</option>
   <option value="Qatar">Qatar</option>
   <option value="Montenegro">Republic of Montenegro</option>
   <option value="serbia">Republic of Serbia</option>
   <option value="Reunion">Reunion</option>
   <option value="Romania">Romania</option>
   <option value="Russia">Russia</option>
   <option value="Rwanda">Rwanda</option>
   <option value="San Marino">San Marino</option>
   <option value="Saudi Arabia">Saudi Arabia</option>
   <option value="Senegal">Senegal</option>
   <option value="Seychelles">Seychelles</option>
   <option value="Sierra Leone">Sierra Leone</option>
   <option value="Singapore">Singapore</option>
   <option value="Slovakia">Slovakia</option>
   <option value="Slovenia">Slovenia</option>
   <option value="Somalia">Somalia</option>
   <option value="South Africa">South Africa</option>
   <option value="Spain">Spain</option>
   <option value="Sri Lanka">Sri Lanka</option>
   <option value="Sudan">Sudan</option>
   <option value="Suriname">Suriname</option>
   <option value="Swaziland">Swaziland</option>
   <option value="Sweden">Sweden</option>
   <option value="Switzerland">Switzerland</option>
   <option value="Syria">Syria</option>
   <option value="Tahiti">Tahiti</option>
   <option value="Taiwan">Taiwan</option>
   <option value="Tajikistan">Tajikistan</option>
   <option value="Tanzania">Tanzania</option>
   <option value="Thailand">Thailand</option>
   <option value="Togo">Togo</option>
   <option value="Tokelau">Tokelau</option>
   <option value="Tonga">Tonga</option>
   <option value="Tobago">Trinidad & Tobago</option>
   <option value="Tunisia">Tunisia</option>
   <option value="Turkey">Turkey</option>
   <option value="Turkmenistan">Turkmenistan</option>
   <option value="Tuvalu">Tuvalu</option>
   <option value="Uganda">Uganda</option>
   <option value="Uk">Uk</option>
   <option value="Ukraine">Ukraine</option>
   <option value="UAE">UAE</option>
   <option value="USA">USA</option>
   <option value="Uraguay">Uruguay</option>
   <option value="Uzbekistan">Uzbekistan</option>
   <option value="Vanuatu">Vanuatu</option>
   <option value="Vatican City ">Vatican City State</option>
   <option value="Venezuela">Venezuela</option>
   <option value="Vietnam">Vietnam</option>
   <option value="Yemen">Yemen</option>
   <option value="DRC">Democratic Republic of Congo</option>
   <option value="Zambia">Zambia</option>
   <option value="Zimbabwe">Zimbabwe</option>
</select>
<br>
<input type="submit" value="submit" class="form-control btn btn-primary btn-block" >

 </form>
 <br>
  <ul class="list-group">
            <li class="list-group-item text-primary">Positive Cases: <span class="badge badge-primary">{{corona.cases}}</span></li>
            <li class="list-group-item text-primary">Today's Cases <span class="badge badge-primary">{{corona.todayCases}}</span></li>
            <li class="list-group-item text-primary">Deaths: <span class="badge badge-primary">{{corona.deaths}}</span></li>
            <li class="list-group-item text-primary">Doday Deaths: <span class="badge badge-primary">{{corona.todayDeaths}}</span></li>
            <li class="list-group-item text-primary">Recovered: <span class="badge badge-primary">{{corona.recovered}}</span></li>
           
            <li class="list-group-item text-primary">Active Cases: <span class="badge badge-primary">{{corona.active}}</span></li>
            <li class="list-group-item text-primary">Critical Cases: <span class="badge badge-primary">{{corona.critical}}</span></li>
            <li class="list-group-item text-primary"> Cases per One Million: <span class="badge badge-primary">{{corona.casesPerOneMillion}}</span></li>
            <li class="list-group-item text-primary">Deaths Per One Million: <span class="badge badge-primary">{{corona.deathsPerOneMillion}}</span></li>
        </ul>
           <h3 class="text-success">Author: Rukundo Jean Claude </h3>
         <div class="container-fluid bg-1 text-center">
  <h3>Who Am I?</h3>
  <img src="../assets/claude.jpg" class="img-circle" alt="Bird">
  <h3>I'm a Web Developper</h3>
</div>

<div class="container-fluid bg-2 text-center">
  <h3>What Am I?</h3>
  <p>I Actually a web developper with a passion of creating my own products</p>
</div>

<div class="container-fluid bg-3 text-center">
  <h3>Where To Find Me?</h3>
  <p class="text-primary"><i class="fa fa-envelope-square fa-2x" aria-hidden="true"></i> rukundocr@gmail.com</p>
  <p class="text-primary"><i class="fa fa-phone fa-2x" aria-hidden="true"></i>+250783289997</p>
</div>
  </div>
 
</template>

<script>
import axios from "axios"
export default {
  name: 'district',
  data () {
    return {
      selected:{},
      corona :{},
      error:'',
      global:{},
      
    options: [
      { text: 'One', value: 'A' },
      { text: 'Two', value: 'B' },
      { text: 'Three', value: 'C' }
    ]

    }
  },
  methods:{
  //-----------------------
  countries(){
      axios.get('https://coronavirus-19-api.herokuapp.com/all')
      .then(response =>{
        this.global = response.data
        console.log(response.data)
      })
    },
  search(e){
      let newsearch = {
        selected:this.selected
      }
      axios.get('https://coronavirus-19-api.herokuapp.com/countries/'+ newsearch.selected)
          .then((response)=>{
           // console.log(response.data)
            this.corona = response.data
            
          })
          .catch((error)=>{
            if(error.response){
            this.error = (error.response.data);}
          })
      e.preventDefault(); 
      
      }
    
  },
   created:function(){
    
      this.countries();
  },
  componets:{
    axios
  }
  

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>