```javascript
function getSyncTime(params) {
  return new Promise((resolve, reject) => {
    try {
      let startTime = new Date().getTime()
      setTimeout(() => {
        let endTime = new Date().getTime()
        let data = endTime - startTime
        resolve( data )
      }, 500)
    } catch ( err ) {
      reject( err )
    }
  });
}

async function getSyncData() {
  let time = await getSyncTime()
  let data = `endTime - startTime = ${time}`
  console.log(data)
}

getSyncData()

```