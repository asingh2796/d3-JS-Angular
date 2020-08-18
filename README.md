 5 steps to get basic D3.JS graph going using Angular 6

## Step 1: Install d3 and type declaration

npm install d3 --save
npm install --save @types/d3

## Step 2: Generate/retrieve chart data 

## Step 3: Pass chart data to shared component which we are creating in step 4.

<app-barchart *ngIf="chartData" [data]="chartData"></app-barchart>

## Step 4: Create shared component like “barchart.component”. In html add div like below.

<div class="d3-chart" #chart></div>

## Step 5-A: Access #chart element using ViewChild

@ViewChild('chart') private chartContainer: ElementRef;

### Step 5-B: On init create chart and append SVG

### Step 5-C: Chart plot area

this.chart = svg.append('g').attr('class', 'bars')

### Step 5-D: Define X and Y, Create Scale, Add colors
