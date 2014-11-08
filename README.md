Easy Chat Commands
============

A simple library for creating Garry's Mod chat commands.

Usage:
-----------

ccmd.AddCommand( command, function( ply, args ) )
Adds a chat command

ccmd.FindPlayerByName( name )
Finds 

Example command
-----------
	ccmd.AddCommand( "example", function( ply, args )
		ply:PrintMessage( HUD_PRINTTALK, "Hi!" )
		if ccmd.FindPlayerByName( args[ 1 ] ) != false then
			ccmd.FindPlayerByName( args[ 1 ] ):PrintMessage( HUD_PRINTTALK, "Hi!" )
		end
		return "The player will say this!"
	end )
	
Output: Prints "Hi!" in chat to the player and the player specifed (if there is one) and makes the player say "The player will say this!"