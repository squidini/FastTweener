<img height="250" src="Documentation/logo.png">


## Description

**FastTweener** - is a one more simple tweener, but **entirely without memory allocation**!

Will be released in AssetStore soon.


Source of inspiration - [DoTween](http://dotween.demigiant.com/). This is realy powerfull and userfreandly tween engine, we use it and love it. But when we faced with extra memory allocation problem we decide to make our own solution, becouse **DoTween is allocate a lot of memory**.

## Benchmarks

<table>
   <tr>
    <th colspan="2"></th>
    <th>DoTween</th>
    <th>FastTweener</th>
   </tr>
   <tr>
   <td rowspan="2"><i>DoTween.Init()</i> vs <i>FastTween.Init()</i>
      <br><sub>For FastTween used pool with 16 base tweens + 16 rigidbody tweens + 16 transform tweens.
      <br>DoTween initialisation containce from <i>DoTween.Init()</i>, <i>DoTween..cctor()</i>, and <i>TweenManager..cctor()</i></sub></td>
   <td>Memory (kb)</td>
   <td>7,9</td>
   <td>5,3</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>6,013</td>
   <td>5,602</td>
   </tr>

   <td rowspan="2">First <i>MonoBehaviour.Update()</i></td>
   <td>Memory (kb)</td>
   <td>0</td>
   <td>0</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>0</td>
   <td>0,482</td>
   </tr>

   <td rowspan="2">Total</td>
   <td>Memory (kb)</td>
   <td>7,9</td>
   <td>5,3</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>6,013</td>
   <td>6,084</td>
   </tr>


   <tr>
   <td colspan="4"></td>
   </tr>

   
   <tr>
   <td rowspan="2"><i>DOVirtual.DelayCall()</i> vs <i>FastTween.Schedule()</i>
      <br><sub>First and second call has a big difference in measures.</sub></td>
   <td>Memory (kb)</td>
   <td>0,8</td>
   <td>0</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>2,19</td>
   <td>0,47</td>
   </tr>

   <td rowspan="2">First <i>MonoBehaviour.Update()</i></td>
   <td>Memory (kb)</td>
   <td>0,136</td>
   <td>0</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>2,77</td>
   <td>0,285</td>
   </tr>
   
   <td rowspan="2">Total</td>
   <td>Memory (kb)</td>
   <td>0,936</td>
   <td>0</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>4,96</td>
   <td>0,755</td>
   </tr>


   <tr>
   <td colspan="4"></td>
   </tr>


   <tr>
   <td rowspan="2"><i>MonoBehaviour.Update()</i> with worked float tween</td>
   <td>Memory (kb)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>


   <tr>
   <td colspan="4"></td>
   </tr>


   <tr>
   <td rowspan="2"><i>On Tween completed</td>
   <td>Memory (kb)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>


   <tr>
   <td colspan="4"></td>
   </tr>


   <tr>
   <td rowspan="2"><i>DOVirtual.DelayCall</i> vs <i>FastTween.Schedule()</i></td>
   <td>Memory (kb)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>

   <td rowspan="2">First <i>MonoBehaviour.Update()</i></td>
   <td>Memory (kb)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>
   
   <td rowspan="2">Total</td>
   <td>Memory (kb)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>


   <tr>
   <td colspan="4"></td>
   </tr>



   <tr>
   <td rowspan="2"><i>MonoBehaviour.Update()</i> with worked scheduling tween</td>
   <td>Memory (kb)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>


   <tr>
   <td colspan="4"></td>
   </tr>


   <tr>
   <td rowspan="2"><i>On Tween completed</td>
   <td>Memory (kb)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>
   <tr>
   <td>Time (ms)</td>
   <td>3,5</td>
   <td>36</td>
   </tr>

</table>

Benchmarks was measured on Apple MacBook Pro 2017.
It was created to show memory allocation difference.
Time metrics is not super-accurate and made only to ensure it not slower than DoTween. 
You can reapeat measures by yourself, all sources are in Benchmark folder.


So, if you don't need all power of DoTween and your goal is memory allocation optimisation - this is plugin for you!



## Benchmarks

Comming soon...
