const { app, BrowserView, BrowserWindow } = require('electron')

app.on('ready', () => {
  const win = new BrowserWindow({ width: 800, height: 600 })

  const view = new BrowserView()
  win.addBrowserView(view)
  win.setBackgroundColor('#ccc')
  view.setBackgroundColor('#fff')
  view.setBounds({ x: 0, y: 0, width: 600, height: 600 })
  view.webContents.loadURL('https://electronjs.org')

  const view2 = new BrowserView()
  win.addBrowserView(view2)
  view2.setBackgroundColor('#FFFFFF')
  view2.setBounds({ x: 200, y: 0, width: 600, height: 600 })
  view2.webContents.loadURL('https://www.qq.com')
})
