# Game Embedded Language

## Sample Code

	class Npc extends GameObject  # GameObject is a class in C++
		function initialize()
			Npc.npcCount = 0
		end
		
		method initialize()
			self.position = Point( 0, 0 )
			Npc.npcCount = Npc.npcCount + 1
		end

		method talk()
		end
	end
	
	class NpcManager
		method initialize()
			# Arrays and dicts are like things in Python
			self.npcs = []
		end

		method addNpc( npc )
			self.npcs.add( npc )
		end

		method addNpc( index, npc )  # Allow function overload with different number of parameters
			self.npcs.insert( index, npc )
		end

		method removeNpc( id )
			# Support lambda just as in C#
			self.npcs.remove( npc => npc.id == id )
		end
	end