import discord
import os

client = discord.Client()


@client.event
async def on_ready():
    print('We have logged in as {0.user}'.format(client))


@client.event
async def on_message(message):
    if message.author == client.user:
        return

    if message.content.startswith('hello'):
        await message.channel.send(
            'Twitter has a disincentive to reduce spam, as it reduces perceived daily users. It is suspicious'
        )

    if message.content.startswith('russia'):
        await message.channel.send(
            'My family fears that the Russians will assassinate me')

    if message.content.startswith('future'):
        await message.channel.send(
            'We’re trying to have the non-weird future get here as fast as possible.'
        )


client.run
    ('OTkxNDkyNzcxODUwNTAyMjI0.GoDv3P.Y8uDYZLtIcES_oPwUmoVniAzIlXbFMFNVAM8jo')
