<script>
  let count = 0
  const increment = () => {
    count += 1
  }
  const openweixin = () => {
    location.assign('weixin://')
  }
  function execCopy(content) {
      var input = document.createElement('input');
      input.setAttribute('value', content);
      input.style.position = 'absolute';
      input.style.width = '1000000';
      input.style.height = '1';
      input.style.opacity = '0';
      input.readOnly = true;
      document.body.appendChild(input);
      input.select();
      input.setSelectionRange(0, 9999);
      console.log('开始写剪贴板', content);
      var rst = document.execCommand('copy');
      console.log('剪贴板写入结果', rst);
      setTimeout(() => {
        document.body.removeChild(input);
      }, 100);
    }
  const openeleme = async () => {
    // location.assign('https://b0994c.ug.ele.me/wow/alsc/mod/9b7dd5e527780fb84b5559a7?inviterId=210db302&actId=1&FastMode=1&_ltracker_f=hjb_app_xbb&chInfo=ch_app_chsub_Photo')
    if(!window.navigator.clipboard) execCopy('0fu置此段 2:/＄daQUkVU＄~.👉饿了么App👈【快來領外賣紅包，最高20元，人人都有哦~】')
    else await window.navigator.clipboard.writeText('0fu置此段 2:/＄daQUkVU＄~.👉饿了么App👈【快來領外賣紅包，最高20元，人人都有哦~】')
    location.assign('eleme://home')
  }
</script>

<button on:click={increment}>
  count is {count}
</button>
<button on:click={openweixin}>
  Open Weixin
</button>
<button on:click={openeleme}>
  Open Eleme
</button>
