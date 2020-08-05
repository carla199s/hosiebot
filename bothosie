import tweepy
import time

consumer_key = 'WtLYJ7qHigPPO8gxq6abRTbPj'

consumer_secret = 'vna2DJ8coLJ1dGmlHPQie7KOzDDlO9EC6TVgc2t66f2RnJ9mnl'

access_token = '3158249711-K7JttrHQkz3a3TgZgXH2AgdAokUFXUfwWobTiVK'
access_token_secret = 'AbAGMwrIWG5s8lU4dW6B9OqLT6UL4l2ofgGGxzIsF102B'


auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)

api = tweepy.API(auth, wait_on_rate_limit=True, wait_on_rate_limit_notify=True)

def main():
    search = ('hosie')
    for tweet in tweepy.Cursor(api.search, search).items(15):
        try:
            tweet.retweet()
            print('Tweet Retweeted')
            time.sleep(10)
        except tweepy.TweepError as e:
            print(e.reason)
        except StopIteration:
            break

main()           
