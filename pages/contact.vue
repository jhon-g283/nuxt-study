<template>
  <!-- 自動でHeaderは読み込まれる。設定用のソースにimportが書いてあるらしいn -->
  <Header />
  <div>
    <div>
      <h1>Contact</h1>
      <p>Please Contact me</p>
      <form method="Post">
        <label htmlFor="name">Name</label>
        <input type="text" name="name" id="name" required />
        <label htmlFor="email">Mail address</label>
        <input type="email" name="email" id="email" required />
        <label htmlFor="textarea">Message</label>
        <textarea name="message" rows="10" id="textarea" required></textarea>
        <button type="submit">送信</button>
      </form>
    </div>
  </div>
  <Footer />
</template>
