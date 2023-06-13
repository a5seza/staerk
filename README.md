# getZKSync
function getZKSyncBalance(address, token) {
  if (['USDC', 'USDT'].includes(token.toUpperCase())) {
    decimal = 6;
  } 
  else {
    decimal = 18;
  }

  var apiUrl = 'https://api.zksync.io/api/v0.2/accounts/' + address;
