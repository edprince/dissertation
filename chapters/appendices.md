\pagebreak

# Appendices

## Appendix A: Evidence of Meetings
![Supervisor Meeting 1](./images/meetings/1.jpg)
![Supervisor Meeting 2](./images/meetings/2.jpg)
![Supervisor Meeting 3](./images/meetings/3.jpg)
![Supervisor Meeting 4](./images/meetings/4.jpg)
![Supervisor Meeting 5](./images/meetings/5.jpg)
![Supervisor Meeting 6](./images/meetings/6.jpg)

## Appendix B: Evidence of Presentation
![Presentation slide](./images/pres_1.png)
![Presentation slide](./images/pres_2.png)
![Presentation slide](./images/pres_3.png)
![Presentation slide](./images/pres_4.png)
![Presentation slide](./images/pres_5.png)
![Presentation slide](./images/pres_6.png)
![Presentation slide](./images/pres_7.png)
![Presentation slide](./images/pres_8.png)
![Presentation slide](./images/pres_9.png)
![Presentation slide](./images/pres_10.png)
![Presentation slide](./images/pres_11.png)
![Presentation slide](./images/pres_12.png)
![Presentation slide](./images/pres_13.png)
![Presentation slide](./images/pres_14.png)
![Presentation slide](./images/pres_15.png)
![Presentation slide](./images/pres_16.png)
![Presentation slide](./images/pres_17.png)
![Presentation slide](./images/pres_18.png)
![Presentation slide](./images/pres_19.png)


## Appendix C: Evidence of Presentation Feedback

![Presentation Feedback \label{presentation_feedback}](./images/meetings/pres.jpg)

\pagebreak

## Appendix D: Experiment Results

## Unbundled Profiling

### At No Throttle


| Run (0x) | Loading (ms) | Scripting (ms) | Rendering (ms) | Painting (ms) | Other (ms) | Idle (ms) |
|----------|--------------|----------------|----------------|---------------|------------|-----------|
| 1        | 4.7          | 3111.8         | 43.4           | 0.6           | 60.9       | 453.4     |
| 2        | 4.1          | 3431.6         | 48.2           | 0.7           | 62.4       | 5100      |
| 3        | 4.8          | 3180.1         | 47.4           | 0.9           | 65.6       | 440.6     |
| 4        | 1            | 3197.6         | 50.7           | 0.4           | 36.1       | 156.2     |
| 5        | 4.7          | 3899.6         | 77.9           | 0.7           | 72.8       | 539.3     |
| 6        | 7            | 3834.2         | 54.9           | 1.3           | 88.1       | 477.8     |
| 7        | 4.9          | 3941.5         | 62.4           | 12.8          | 83.9       | 617.5     |
| 8        | 5.3          | 3694.9         | 53.2           | 1.4           | 94.1       | 515.8     |
| 9        | 5.2          | 4164.4         | 59.1           | 0.7           | 84.2       | 670.3     |
| 10       | 5.7          | 3434.5         | 59.3           | 3             | 157        | 804.3     |
| 11       | 4.6          | 3581.2         | 55.8           | 2.6           | 77.2       | 682.4     |
| 12       | 4.2          | 3206.8         | 45.5           | 0.6           | 71.9       | 524.1     |
| 13       | 5.8          | 4151.7         | 53.5           | 0.7           | 88.5       | 500.6     |
| 14       | 4.1          | 4656.3         | 59.2           | 0.8           | 78.9       | 555.5     |
| 15       | 12           | 4185.6         | 57.1           | 1.2           | 80.9       | 664.8     |
| 16       | 4.2          | 3698.1         | 51.7           | 1.1           | 84.2       | 492.3     |
| 17       | 4.3          | 3724.6         | 49.5           | 2.6           | 78.6       | 496.5     |
| 18       | 5.4          | 3618.6         | 53.3           | 0.9           | 83.2       | 496.6     |
| 19       | 5.4          | 4018.2         | 57.1           | 1             | 85.8       | 525       |
| 20       | 4.6          | 3551.9         | 50.9           | 0.7           | 82.7       | 490.1     |
| Average  | 5.1          | 3714.16        | 54.505         | 1.735         | 80.85      | 760.155   |

Table: Unbundled at No Throttle \label{unbundled_0x}

### At 4x Throttle

| Run (4x) | Loading (ms) | Scripting (ms) | Rendering (ms) | Painting (ms) | Other (ms) | Idle (ms) |
|----------|--------------|----------------|----------------|---------------|------------|-----------|
| 1        | 15.5         | 12827.6        | 164.2          | 2.1           | 186.8      | 645.7     |
| 2        | 6.2          | 10566.3        | 159.9          | 1.9           | 214.1      | 734.5     |
| 3        | 12.9         | 13499          | 155.4          | 2.1           | 205.1      | 671       |
| 4        | 19.8         | 12701.8        | 155.1          | 2.2           | 193.6      | 898       |
| 5        | 10.7         | 9852.5         | 187.1          | 6.7           | 372        | 713.9     |
| 6        | 11           | 12833.3        | 178.4          | 7.9           | 261.2      | 947.5     |
| 7        | 7.2          | 11398          | 180.7          | 6.7           | 290.4      | 661.1     |
| 8        | 16.1         | 12382.4        | 165.8          | 2.4           | 192.2      | 799.7     |
| 9        | 12.1         | 12313.2        | 181.9          | 2.3           | 313.2      | 932.5     |
| 10       | 15.8         | 14077.1        | 180.6          | 2.1           | 274.5      | 750.2     |
| 11       | 18.3         | 7225.1         | 169.9          | 2.3           | 190.4      | 774.6     |
| 12       | 9.3          | 13893.1        | 187.2          | 2.4           | 121.5      | 594.6     |
| 13       | 13.2         | 13131.3        | 199.9          | 5.2           | 234.9      | 789.8     |
| 14       | 9.8          | 14363.4        | 167.2          | 1.7           | 199.9      | 967.2     |
| 15       | 19           | 11134.7        | 168.8          | 6.6           | 219        | 553       |
| 16       | 19.5         | 12194.9        | 177.9          | 3.7           | 235        | 627.1     |
| 17       | 11.8         | 12514.6        | 187            | 2.8           | 186.3      | 942.6     |
| 18       | 14.6         | 12724.4        | 160.5          | 3             | 282.4      | 797.2     |
| 19       | 26.1         | 15305.5        | 172.1          | 3.2           | 398        | 816.5     |
| 20       | 16.3         | 12208.5        | 176.5          | 6.3           | 242.7      | 584.7     |
| Average  | 14.26        | 12357.335      | 173.805        | 3.68          | 240.66     | 760.07    |

Table: Unbundled at 4x Throttle \label{unbundled_4x}


### At 6x Throttle

| Run (6x) | Loading (ms) | Scripting (ms) | Rendering (ms) | Painting (ms) | Other (ms) | Idle (ms) |
|----------|--------------|----------------|----------------|---------------|------------|-----------|
| 1        | 8.5          | 19643.1        | 211.8          | 2.4           | 246.7      | 577.7     |
| 2        | 6.4          | 14932.7        | 191.6          | 2.6           | 644.9      | 631.9     |
| 3        | 23.7         | 19366.7        | 254.1          | 3.3           | 244.1      | 552.2     |
| 4        | 18.3         | 19754.3        | 184.8          | 4.3           | 351.3      | 538       |
| 5        | 11.4         | 19008.9        | 227.9          | 2.9           | 715.7      | 668.5     |
| 6        | 25.9         | 21328.3        | 108.5          | 14.9          | 1622.9     | 1117.2    |
| 7        | 9.6          | 14051.8        | 239.6          | 3.1           | 365        | 1273.9    |
| 8        | 9.2          | 19393.9        | 188.9          | 4.9           | 334.8      | 715.2     |
| 9        | 17.5         | 21682.2        | 271.2          | 4.1           | 529.6      | 980.9     |
| 10       | 21.3         | 22173.7        | 243.6          | 4             | 835.8      | 851.5     |
| 11       | 9.2          | 17532.4        | 256            | 4.4           | 320.8      | 921.1     |
| 12       | 8.2          | 19373.5        | 251.3          | 2.7           | 213.5      | 654.6     |
| 13       | 8            | 17301          | 224.3          | 1.8           | 387.6      | 1423.8    |
| 14       | 11.2         | 20298.6        | 118            | 2.9           | 512.2      | 1036.1    |
| 15       | 11.5         | 16325          | 232.9          | 10.1          | 220.3      | 797.8     |
| 16       | 9.8          | 18459.1        | 178.3          | 1.4           | 303.8      | 684.5     |
| 17       | 22.3         | 18405.5        | 380.6          | 3.9           | 249.3      | 852.9     |
| 18       | 28.6         | 19070.7        | 224.5          | 1.9           | 1249.2     | 562.1     |
| 19       | 15.2         | 13584.4        | 177.1          | 1.1           | 307.5      | 794.6     |
| 20       | 10.1         | 20168.3        | 260            | 3.1           | 319        | 662.9     |
| Average  | 14.295       | 18592.705      | 221.25         | 3.99          | 498.7      | 814.87    |

Table: Unbundled at 6x Throttle \label{unbundled_6x}

## React Webpack

### At No Throttle


| Run (0x) | Loading (ms) | Scripting (ms) | Rendering (ms) | Painting (ms) | Other (ms) | Idle (ms) |
|----------|--------------|----------------|----------------|---------------|------------|-----------|
|  1 | 12.2 | 2852.9 | 54.7 | 1.3 | 45.9 | 524.6 |
|  2 | 13.1 | 3011.8 | 67.6 | 1.0 | 41.6 | 466.0 |
|  3 | 13.4 | 2916.5 | 52.7 | 1.0 | 43.3 | 465.9 |
|  4 | 12.1 | 2790.0 | 51.6 | 0.7 | 41.5 | 479.0 |
|  5 | 13.5 | 2952.6 | 54.9 | 0.8 | 43.3 | 500.5 |
|  6 | 13.6 | 2769.9 | 55.6 | 0.8 | 41.6 | 558.1 |
|  7 | 13.8 | 2935.2 | 53.6 | 0.9 | 57.3 | 454.2 |
|  8 | 11.2 | 2869.7 | 56.3 | 0.8 | 50.4 | 520.7 |
|  9 | 13.2 | 3969.4 | 51.3 | 0.6 | 48.9 | 568.5 |
|  10 | 13.5 | 2838.4 | 52.9 | 0.8 | 45.2 | 436.2 |
|  11 | 13 | 2867 | 54.7 | 0.8 | 42.7 | 454.7 |
|  12 | 12.8 | 2826.9 | 50 | 0.6 | 46 | 492.1 |
|  13 | 12.1 | 2902.6 | 50.5 | 0.9 | 45.8 | 490.6 |
|  14 | 12.5 | 2929.5 | 50.7 | 1 | 46.1 | 469.7 |
|  15 | 12.2 | 2960.9 | 58.4 | 0.7 | 43.5 | 573.8 |
|  16 | 13.2 | 2844.5 | 50.3 | 1.2 | 55.6 | 476.6 |
|  17 | 11.9 | 2934.4 | 51.4 | 0.7 | 42.5 | 475.6 |
|  18 | 12.5 | 2965.1 | 51.5 | 0.7 | 43.8 | 450.5 |
|  19 | 13.2 | 2968.4 | 52.2 | 1.4 | 48.4 | 438.2 |
|  20 | 12.7 | 2930.3 | 52.6 | 1 | 45.1 | 471.6 |
|  Average | 12.785 | 2951.8 | 53.675 | 0.885 | 45.925 | 488.355 |

Table: Bundled at No Throttle \label{webpack_0x}

### At 4x Throttle

| Run (4x) | Loading (ms) | Scripting (ms) | Rendering (ms) | Painting (ms) | Other (ms) | Idle (ms) |
|----------|--------------|----------------|----------------|---------------|------------|-----------|
|  1 | 21 | 12102.7 | 180.8 | 3.4 | 91.2 | 638.8 |
|  2 | 55.2 | 10741.4 | 186 | 0.2 | 228.3 | 401.6 |
|  3 | 41.4 | 10910.9 | 176 | 1.8 | 106.8 | 431.7 |
|  4 | 58.4 | 12146.9 | 184.8 | 0.6 | 86.3 | 509.5 |
|  5 | 40.3 | 10720.5 | 181.9 | 0.8 | 97.9 | 454.6 |
|  6 | 42.2 | 11731.6 | 184.5 | 1.6 | 102.2 | 503.4 |
|  7 | 40.4 | 11037.4 | 196 | 0.6 | 99.4 | 495 |
|  8 | 32.3 | 12096.9 | 188.9 | 1.3 | 78 | 515.9 |
|  9 | 34.2 | 11619.8 | 179.9 | 0.5 | 119.5 | 649 |
|  10 | 38.7 | 11833.5 | 174.1 | 0.5 | 156.8 | 529 |
|  11 | 35.2 | 11706.1 | 178.4 | 0.7 | 131.6 | 445.2 |
|  12 | 44.7 | 12340.6 | 193.7 | 6.4 | 132.9 | 446.4 |
|  13 | 101.3 | 12052.7 | 172.7 | 1 | 85 | 422.4 |
|  14 | 64.2 | 11944.8 | 190.9 | 1.3 | 91.5 | 542.7 |
|  15 | 51.8 | 11049.8 | 179.3 | 0.4 | 86.6 | 482.5 |
|  16 | 45.5 | 12259.8 | 187.5 | 0.3 | 80.3 | 430.5 |
|  17 | 47.1 | 11224.3 | 182.4 | 2 | 172.3 | 434 |
|  18 | 43.5 | 11544.7 | 188.6 | 1.4 | 108 | 405.9 |
|  19 | 26.9 | 11722.5 | 184.7 | 2.3 | 112.6 | 529.3 |
|  20 | 34.7 | 11774.3 | 181 | 0.8 | 120.8 | 510.6 |
|  Average | 44.95 | 11628.06 | 183.605 | 1.395 | 114.4 | 488.9 |


Table: Bundled at 4x Throttle \label{webpack_4x}

### At 6x Throttle

| Run (6x) | Loading (ms) | Scripting (ms) | Rendering (ms) | Painting (ms) | Other (ms) | Idle (ms) |
|----------|--------------|----------------|----------------|---------------|------------|-----------|
|  1 | 58.7 | 18068.7 | 166.6 | 2.6 | 198 | 472.7 |
|  2 | 54.8 | 18064.4 | 269.8 | 0.4 | 442.1 | 467.8 |
|  3 | 25.8 | 16431.1 | 218.1 | 7 | 113.9 | 482.1 |
|  4 | 51.3 | 18038 | 228.6 | 1 | 242.2 | 447.1 |
|  5 | 39.2 | 16284.8 | 226.5 | 5.5 | 114.6 | 570.7 |
|  6 | 43.7 | 18446.5 | 360.7 | 3 | 340.1 | 355.3 |
|  7 | 64.2 | 16201.7 | 234.2 | 2.2 | 370.6 | 559.4 |
|  8 | 32.5 | 18417.2 | 255.2 | 7 | 179 | 389.6 |
|  9 | 93.8 | 16435.9 | 229.9 | 1.8 | 208.8 | 530.6 |
|  10 | 24 | 17649.1 | 216.2 | 0.4 | 175.8 | 470.5 |
|  11 | 88.5 | 17280.8 | 216.9 | 3.3 | 200.7 | 422.4 |
|  12 | 30.3 | 17540.1 | 220.3 | 1.6 | 216.1 | 525.5 |
|  13 | 109.3 | 18272.8 | 381.6 | 7.3 | 253.3 | 406 |
|  14 | 46 | 17913.8 | 245.8 | 2.1 | 250.7 | 510.1 |
|  15 | 81.5 | 16256.5 | 236.4 | 0.7 | 122.8 | 570.3 |
|  16 | 26.4 | 18408.6 | 136 | 0.3 | 261.7 | 493.8 |
|  17 | 46.1 | 16755.5 | 223.5 | 0.4 | 133.4 | 451.9 |
|  18 | 39.8 | 17334.5 | 246 | 0.9 | 160.4 | 454 |
|  19 | 37.8 | 16258.8 | 211.5 | 0.4 | 95.8 | 456.7 |
|  20 | 35.8 | 18704.1 | 223.3 | 0.8 | 199.4 | 386.3 |
|  Average | 51.475 | 17438.145 | 237.355 | 2.435 | 213.97 | 471.14 |

Table: Bundled at 6x Throttle \label{webpack_6x}

## Appendix E: Automation Code

```javascript
const puppeteer = require('puppeteer');
let i = 0;
const DIR = 'hyperapp-rollup';
const URL = 'http://localhost:5000';

let loop = setInterval(async () => {
    if (i === 19) {
        clearInterval(loop);
    }
    throttleSix(i);
    throttleFour(i);
    throttleNone(i);
    i++;
}, 20000)

async function throttleSix(i) {
    const browser = await puppeteer.launch();
    const page = await browser.newPage();
    const client = await page.target().createCDPSession();
    await client.send('Emulation.setCPUThrottlingRate', { rate: 6 });
    await page.tracing.start({ path: `traces/${DIR}/6x/${i}profile-${Date.now()}.json` });
    await page.goto(URL);
    await page.tracing.stop();
    await browser.close();
}

async function throttleFour(i) {
    const browser = await puppeteer.launch();
    const page = await browser.newPage();
    const client = await page.target().createCDPSession();
    await client.send('Emulation.setCPUThrottlingRate', { rate: 4 });
    await page.tracing.start({ path: `traces/${DIR}/4x/${i}profile-${Date.now()}.json` });
    await page.goto(URL);
    await page.tracing.stop();
    await browser.close();
}

async function throttleNone(i) {
    const browser = await puppeteer.launch();
    const page = await browser.newPage();
    const client = await page.target().createCDPSession();
    await page.tracing.start({ path: `traces/${DIR}/0x/${i}profile-${Date.now()}.json` });
    await page.goto(URL);
    await page.tracing.stop();
    await browser.close();
}
```