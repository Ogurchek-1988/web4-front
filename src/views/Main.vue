<template>
    <div id="home" >

         <div  class="left">
         <div class="image-container">
             <h2>Graph </h2>
             <svg class="graph" viewBox="-100 -100 200 200" xmlns="http://www.w3.org/2000/svg" @click="sendPointFromSvg">
                        <defs>
                            <marker id='arrow-head' orient="auto"
                                    markerWidth='2' markerHeight='4'
                                    refX='0.1' refY='2'>
                                <path d='M0,0 V4 L2,2 Z' fill="black"></path>
                            </marker>
                        </defs>
                        <polygon class="triangle" points="0 0, 0 40, -20 0" fill="rgb(0, 160, 223)"></polygon>
                        <rect class="rectangle" x="0" y="0" width="20" height="40" fill="rgb(0, 160, 223)"></rect>
                        <path class="circle" fill="rgb(0, 160, 223)" d="M 0 0 h 20 C 20 0 20 -20 0 -20"></path>
                        <path
                                d="M -95 0, h 190"
                                stroke="black"
                                stroke-width="1"
                                marker-end="url(#arrow-head)"></path>
                        <path
                                d="M 0 95, v -190"
                                stroke="black"
                                stroke-width="1"
                                marker-end="url(#arrow-head)"></path>
                        <text x="92" y="-3" class="graph__inscription">x</text>
                        <text x="3" y="-92" class="graph__inscription">y</text>
                        <text x="12" y="-3" class="graph__inscription">R/2</text>
                        <text x="-31" y="-3" class="graph__inscription">-R/2</text>
                        <text x="3" y="23" class="graph__inscription">-R/2</text>
                        <text x="3" y="-17" class="graph__inscription">R/2</text> 
                        <text x="37" y="-3" class="graph__inscription">R</text>
                        <text x="-47" y="-3" class="graph__inscription">-R</text>
                        <text x="3" y="43" class="graph__inscription">-R</text>
                        <text x="3" y="-37" class="graph__inscription">R</text>

                        <circle cx="0" cy="0" r="1.5" fill="black"></circle>
                        <circle cx="0" cy="20" r="1.5" fill="black"></circle>
                        <circle cx="0" cy="-20" r="1.5" fill="black"></circle>
                        <circle cx="20" cy="0" r="1.5" fill="black"></circle>
                        <circle cx="-20" cy="0" r="1.5" fill="black"></circle>
                        <circle cx="40" cy="0" r="1.5" fill="black"></circle>
                        <circle cx="-40" cy="0" r="1.5" fill="black"></circle>
                        <circle cx="0" cy="40" r="1.5" fill="black"></circle>
                        <circle cx="0" cy="-40" r="1.5" fill="black"></circle>
                    </svg>
         </div>
     </div >


          <div  class="right">
              <h2 style="text-align: center">Input Data From here: </h2>
                  <div class="X-input">
                      <label class="lable_xyr">X: </label>

                      <input class="x-radio" id="x-radio1" type="radio" name="xval" value="-4" v-model="x">
                      <label class="xbox-label" for="x-radio1">-4</label>

                      <input class="x-radio" id="x-radio2" type="radio" name="xval" value="-3" v-model="x">
                      <label class="xbox-label" for="x-radio2">-3</label>

                      <input class="x-radio" id="x-radio3" type="radio" name="xval" value="-2" v-model="x">
                      <label class="xbox-label" for="x-radio3">-2</label>

                      <input class="x-radio" id="x-radio4" type="radio" name="xval" value="-1" v-model="x">
                      <label class="xbox-label" for="x-radio4">-1</label>

                      <input class="x-radio" id="x-radio5" type="radio" name="xval" value="0" v-model="x">
                      <label class="xbox-label" for="x-radio5">0</label>

                      <input class="x-radio" id="x-radio6" type="radio" name="xval" value="1" v-model="x">
                      <label class="xbox-label" for="x-radio6">1</label>

                      <input class="x-radio" id="x-radio7" type="radio" name="xval" value="2" v-model="x">
                      <label class="xbox-label" for="x-radio7">2</label>

                      <input class="x-radio" id="x-radio8" type="radio" name="xval" value="3" v-model="x">
                      <label class="xbox-label" for="x-radio8">3</label>

                      <input class="x-radio" id="x-radio9" type="radio" name="xval" value="4" v-model="x">
                      <label class="xbox-label" for="x-radio9">4</label>
                  </div>
                  <br>
                  <div class="Y-Input">
                      <label class="lable_xyr label_y">Y:  </label>
                      <input id="y-textinput" type="text" name="yval" maxlength="9" autocomplete="off" placeholder="Number from -3 to 3" v-model="y">
                  </div>
                  <br>

                  <div class="R-input">
                      <label class="lable_xyr">R: </label>

                      <input class="x-radio" id="r-radio1" type="radio" name="rval" value="-4" v-model="r">
                      <label class="xbox-label" for="r-radio1">-4</label>

                      <input class="x-radio" id="r-radio2" type="radio" name="rval" value="-3" v-model="r">
                      <label class="xbox-label" for="r-radio2">-3</label>

                      <input class="x-radio" id="r-radio3" type="radio" name="rval" value="-2" v-model="r">
                      <label class="xbox-label" for="r-radio3">-2</label>

                      <input class="x-radio" id="r-radio4" type="radio" name="rval" value="-1" v-model="r">
                      <label class="xbox-label" for="r-radio4">-1</label>

                      <input class="x-radio" id="r-radio5" type="radio" name="rval" value="0" v-model="r">
                      <label class="xbox-label" for="r-radio5">0</label>

                      <input class="x-radio" id="r-radio6" type="radio" name="rval" value="1" v-model="r">
                      <label class="xbox-label" for="r-radio6">1</label>

                      <input class="x-radio" id="r-radio7" type="radio" name="rval" value="2" v-model="r">
                      <label class="xbox-label" for="r-radio7">2</label>

                      <input class="x-radio" id="r-radio8" type="radio" name="rval" value="3" v-model="r">
                      <label class="xbox-label" for="r-radio8">3</label>

                      <input class="x-radio" id="r-radio9" type="radio" name="rval" value="4" v-model="r">
                      <label class="xbox-label" for="r-radio9">4</label>

                      <div class="buttons">
                          <button class="button-submit" type="submit" name="Submit" @click="submitForm">Submit</button>
                          <button class="button-reset" type="reset" name="Reset" @click="resetPoints">Reset</button>
                          <button class="button-logout" name="logout" @click="logout">Logout</button>
                      </div>
                  </div>
          </div>
        </div>

        <div id="maintable">
            <div class="table">
               <table style="width: 100%">
                   <br>
                       <div class="plate-top">
                           <h2 class="plate-top-title"> Table </h2>
                       </div>

                       <div class="scroll-container">
                           <table id="result-table">
                               <tr class="table-header">
                                   <th class="coords-col"> X </th>
                                   <th class="coords-col">Y</th>
                                   <th class="coords-col">R</th>
                                   <th class="hitres-col"> Hit result</th>
                                   <th class="time-col"> Excution time</th>
                               </tr>
                                <tr v-for="point in points" :key="point">
                                    <td class="coords-col">{{point.x.toFixed(3)}}</td>
                                    <td class="coords-col">{{point.y.toFixed(3)}}</td>
                                    <td class="coords-col">{{point.r}}</td>
                                    <td class="hitres-col">{{point.hitResult}}</td>
                                    <td class="time-col">{{point.time}}</td>
                                </tr>
                           </table>
                       </div>
               </table>
            </div>
        </div>
</template>

<script>
export default {
    name: "Main",
    data(){
        return {
            x: "-4",
            y: "-3",
            r: "-4",
            points: new Array()
        }
    },
    watch: {
        y(value) {
            const buttonSubmit = document.querySelector(".button-submit");
            const yTextInput = document.querySelector(".label_y");
            if (!isNaN(parseFloat(value)) && isFinite(value) && value <= 3 && value >= -3) {
                buttonSubmit.disabled = false;
                buttonSubmit.style.border = "2px solid #c5e29a"
                yTextInput.style.backgroundColor = "#060e1b"
            } else {
                buttonSubmit.disabled = true;
                buttonSubmit.style.border = "2px solid #B00020";
                yTextInput.style.backgroundColor = "#B00020"
            }
        
        },
        r(value) {
            const rectangle = document.querySelector('.rectangle')
            document.querySelector('.triangle').setAttribute("points", `0 0, 0 ${40*value}, ${-20*value} 0`);
            document.querySelector('.circle').setAttribute("d", `M 0 0 h ${20*value} C ${20*value} 0 ${20*value} ${-20*value} 0 ${-20*value}`);
            rectangle.setAttribute("y", 0 * value);
            rectangle.setAttribute("width", 20 * value);
            rectangle.setAttribute("height", 40 * value);
        }
    },
    methods: {
        submitForm(event) {
            event.preventDefault();
            const userDetails = JSON.parse(localStorage.getItem("userDetails"));
            if (userDetails) {
                this.axios.post('/api/points/check', {
                    x: this.x,
                    y: this.y,
                    r: this.r
                },
                {
                    headers: {"Authorization": "Bearer " + userDetails.accessToken}
                }).then(() => {
                    this.getPoints();
                }).catch(error => {
                    if (error.response.status == 401 || error.response.status == 403) {
                        this.invalidateTokenAndGoToAuthPage();
                    }
                })
            } else this.invalidateTokenAndGoToAuthPage();
        },
        resetPoints(event) {
            event.preventDefault();
            const userDetails = JSON.parse(localStorage.getItem("userDetails"));
            this.axios.delete("/api/points/clear",
            {
                headers: {"Authorization": "Bearer " + userDetails.accessToken}
            }).then(() => {
                this.getPoints();
                this.drawPoints();
            }).catch(error => {
                if (error.response.status == 401 || error.response.status == 403) {
                    this.invalidateTokenAndGoToAuthPage();
                }
            })
        },
        getPoints() {
            const userDetails = JSON.parse(localStorage.getItem("userDetails"));
            this.axios.get("/api/points/get", {
                headers: {"Authorization": "Bearer " + userDetails.accessToken}
            }).then(response => {
                console.log(response.data);
                this.points = [];
                for (const p of response.data) {
                  this.points.push({x: p.coordinateX, y: p.coordinateY, r: p.radius, hitResult: p.hit, time: p.time})
                }
                // this.points = response.data;
                this.drawPoints();
            }).catch(error => {
                alert(error.message);
                if (error.response.status == 401 || error.response.status == 403) {
                    this.invalidateTokenAndGoToAuthPage();
                }
            })
        },
        getPointsListFromResponse(json) {
            let pointsUnwraped = new Array();
            if (json._embedded !== undefined) {
                for (let jsonObj of json._embedded.pointList) {
                    pointsUnwraped.push((({ x, y, r, hitResult, time }) => ({ x, y, r, hitResult, time }))(jsonObj))
                }
            }
            return pointsUnwraped;
        },
        invalidateTokenAndGoToAuthPage() {
            localStorage.removeItem("userDetails");
            this.$router.push({name: "auth"});
        },
        drawPoints() {
          const svg = document.querySelector('.graph');
          document.querySelectorAll('.circle--point').forEach(point => point.remove());

          if (this.points) {
            for (let point of this.points) {
                const circleElement = document.createElementNS("http://www.w3.org/2000/svg", "circle");
                circleElement.classList.add('circle--point');
                circleElement.setAttribute("cx", point.x*40);
                circleElement.setAttribute("cy", -point.y*40);
                circleElement.setAttribute("r", 1);
                circleElement.setAttribute("fill", point.hitResult ? "green" : "red");
                svg.appendChild(circleElement);
            }
          }
        },
        sendPointFromSvg(event) {
            event.preventDefault();
            const svg = document.querySelector('.graph');
            const pt = svg.createSVGPoint();

            pt.x = event.clientX;
            pt.y = event.clientY;
            let loc = pt.matrixTransform(svg.getScreenCTM().inverse());

            let xSvg = loc.x/40;
            let ySvg = -loc.y/40;

            this.axios.post("/api/points/check", {
                x: xSvg,
                y: ySvg,
                r: this.r
            },
            {
                headers: {"Authorization": "Bearer " + JSON.parse(localStorage.getItem("userDetails")).accessToken}
            }).then(() => {
                this.getPoints();
            }).catch(error => {
                if (error.response.status == 401) {
                    this.invalidateTokenAndGoToAuthPage();
                }
            })
        },
        logout(event) {
            event.preventDefault();
            localStorage.removeItem("userDetails");
            this.$router.push({name: "auth"});
        }
    }
}

</script>

<style scoped>
#home{
    width: 100%;
    display: flex;
    flex-direction: row-reverse;

}

.left{
    background-color: #275179;
    width: 50%;
    float: right;
    margin-top: 0.5%;
    text-align: center;
    border: 2px solid #060e1b;
    /*border: 2px solid #060e1b;*/
  /*margin-top: 8%;*/
  margin-left: 1%;
  border-radius: 6%;
  padding: 1% 1%;

}

.right{
    background-color: #275179;
    width: 50%;
    margin-top: 0.5%;
    margin-right: 1%;
    float: left;
    border: solid 2px;
    height: auto;
    padding: 1%;
     border: 2px solid #060e1b;
    /*border: 2px solid #060e1b;*/
  /*margin-right: 2%;*/
  border-radius: 6%;
  padding: 1% 1%;
}

.left_head{
    width: 50%;
    float: left;
    padding: 1%;

}

.right_head{
    width: 43%;
    float: right;
    text-align: right;
    padding: 1%;




}
body{
    background-color: #564F6F;
    color: whitesmoke;


    /*margin-left: 20px;*/
    /*margin-right: 30px;*/
    /*width: auto;*/

}
.lable_xyr{
    background-color: #060e1b;
    /*padding: 1%;*/
    margin-right: 2%;
    color: #ffffff;
  margin-top: 6%;
  margin-left: 3%;
  border-radius: 28%;
  padding: 1% 1%;
}

button {
    margin-top: 8%;
    margin-left: 5%;
    border-radius: 30%;
    padding: 2% 2%;
    border: 2px solid #060e1b;
    position: relative;
    overflow: hidden;
    background-color: transparent;
    text-align: center;
    text-transform: uppercase;
    font-size: 14px;
    color: #ddd;
    transition: .3s;
    z-index: 1;
    font-family: inherit;
    color: whitesmoke;
}

button::before {
    content: '';
    width: 0;
    height: 300%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) rotate(45deg);
    background: #060e1b;
    transition: .5s ease;
    display: block;
    z-index: -1;
}

button:hover::before {
    width: 105%;
}

button:hover {
    color: #111;
}

.content-plate {
    padding: 0 0 10%;
    vertical-align: top;
    background-color: #ffffff;
}

.plate-top {
    display: inline-block;
    width: 100%;
    /*margin: 0;*/
    /*margin-bottom: 20px;*/
    padding: 0em 0;
    text-align: center;
    color: #ffffff;
    background-color: #112030;
}

.plate-top-title {
    font-size: 18px;
    font-weight: normal;
}
#table-plate {
    position: relative;
}

.scroll-container {
    /*position: relative;*/
    /*bottom: 0;*/
    /*right: 0;*/
    /*top: 54px;*/
    width: 100%;
    /*overflow-y: scroll;*/
}

#result-table {
    width: 100%;
    text-align: center;
  color: #ffffff;
    /*border-collapse: collapse;*/
}

#result-table tr {
    height: 4%;
}

#result-table tr:nth-child(2n-1) {
    background-color: #112030;
}

#result-table tr:nth-child(2n):hover {
    background-color: #e9e9e9;
}

#result-table tr:nth-child(2n-1):hover {
    background-color: #112030
}

#result-table tr.table-header:hover {
    background-color: #112030;
}

.coords-col {
    width: 12%;
}

.time-col {
    width: 25%;
}
#y-textinput{
    width: calc(100% - 50%);
}

@media(max-width: 819px) {
    .graph{
        /*height: auto;*/
        /*width: auto;*/
        /*overflow: auto;*/
        /*resize: both;*/
        /*position: -ms-device-fixed;*/
        /* max-width: 60% */
        max-width: 200px;
        max-height: 200px;
    }
}

.graph{
        /*height: auto;*/
        /*width: auto;*/
        /*overflow: auto;*/
        /*resize: both;*/
        /*position: -ms-device-fixed;*/
        /* max-width: 60% */
        max-width: 300px;
        max-height: 300px;
    }

.graph__inscription{
    font-size:9px;
    font-family:-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-style: normal;
}

</style>