# TEST CONDITIONS
- 1080p
- Slight overclock (+49MHz GPU, +200MHz VRAM)
- Xbox Store game
- Ran with all my background apps (it shouldn't affect performance, but still)
## High Preset Tests
| AA/Upscaling Tech | Average FPS | 1% Low FPS |
|:-------------:|:-------------:|:-------------:|
| MSAA x2 | 81 | 65 |
| MSAA x4 | 78 | 63 |
| MSAA x8 | 74 | 60 |
| FSR Quality | 77 | 62 |
| FSR Balanced | 80 | 65 |
| XeSS Quality | 73 | 61 |
| XeSS Balanced | 75 | 62 |

## Ultra Preset Tests
| AA/Upscaling Tech | Average FPS | 1% Low FPS |
|:-------------:|:-------------:|:-------------:|
| MSAA x2 | 60 | 46 |
| MSAA x4 | 59 | 46 |
| MSAA x8 | 54 | 41 |
| FSR Quality | 58 | 48 |
| FSR Balanced | 57 | 48 |
| XeSS Quality | 48 | 37 |
| XeSS Balanced | 51 | 41 |

## What does that mean?
You might ask: Are upscaling techniques supposed to improve performance? Yes, but not in 100% of cases

My poor GTX 1660 Super is being hammered by this game, it runs at nearly 100%. And all the upscalers must calculate what pixels might be if the image was rendered at native res, and these calculations use performance, and in those cases, the performance gain (for rendering the game at a lower resolution) is so little that all the upscaling process uses all the performance gain, and even more (that's why there are lower fps on FSR/XeSS than native rendering)

And as for XeSS, is uses AI even on non AI accelerated GPUs (such as GTX cards), and because GTX cards don't have dedicated AI cores, XeSS must use CUDA cores, and those CUDA cores are also rendering the game, so the same thing happens (even worse) 

### How can we use upscaling to improve performance?
With this GPU? I don't think so. Because we would need to lower the graphics settings (on medium preset for example) to lower the GPU usage. But at some point you will reach your max screen refresh rate (in my case 100 Hz), and there's no need to improve performance if you can't benefit from this performance gain. But if you have a second GPU lying around (a dedicated one, or your iGPU if you have one) you can upscale your game using it with Lossless Scaling (without performance cost on the main GPU) (I won't detail how all of this works, but there are plenty of videos/guides on the internet to help you out (such as LTT's video))
